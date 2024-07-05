<template>
  <div>
    <BadgeDisplay :name="badgeName" :solution="badgeSolution" :icon="badgeIcon" :reward="badgeReward" :isSkill="badgeIsSkill" :obtainable="badgeObtainable" />
  </div>
</template>

<script lang="ts" setup>
const route = useRoute()

import bbBadges from '../../../public/assets/badges/list/bb.json';
import dbBadges from '../../../public/assets/badges/list/db.json';
import generalBadges from '../../../public/assets/badges/list/general.json';
import hitwBadges from '../../../public/assets/badges/list/hitw.json';
import pkwBadges from '../../../public/assets/badges/list/pkw.json';
import rsrBadges from '../../../public/assets/badges/list/rsr.json';
import sbBadges from '../../../public/assets/badges/list/sb.json';
import tgttosBadges from '../../../public/assets/badges/list/tgttos.json';

var badges = generalBadges

switch (route.params.gameType) {
  case 'bb':
    badges = bbBadges
    break;
  
  case 'db':
    badges = dbBadges
    break;

  case 'hitw':
    badges = hitwBadges
    break;
  
  case 'pkw':
    badges = pkwBadges
    break;
  
  case 'rsr':
    badges = rsrBadges
    break;

  case 'sb':
    badges = sbBadges
    break;

  case 'tgttos':
    badges = tgttosBadges
    break;

  default:
    break;
}

var badgeName: String = ""
var badgeSolution: String = ""
var badgeIcon: String = ""
var badgeReward: Number = 0
var badgeIsSkill: Boolean = true
var badgeObtainable = ref(false)

for (let index = 0; index < badges.length; index++) {
  if (badges[index].id == route.params.id) {
    badgeName = badges[index].label
    badgeSolution = badges[index].solution
    badgeIcon = badges[index].badgeIcon
    badgeReward = badges[index].reward
    badgeIsSkill = badges[index].isSkill
    badgeObtainable.value = badges[index].obtainable
  }
}
</script>

<style></style>