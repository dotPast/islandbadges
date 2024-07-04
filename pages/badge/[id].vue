<template>
  <div>
    <BadgeDisplay :name="badgeName" :icon="badgeIcon" :description="badgeDesc" :solution="badgeSolution" />
  </div>
</template>

<script lang="ts" setup>
const route = useRoute()
var foundBadge = false
var badgeName: String
var badgeDesc: String
var badgeSolution: String
var badgeIcon: String

import json from '../../public/assets/badges.json';

for (let index = 0; index < json.length; index++) {
  if (json[index].id == route.params.id) {
    badgeName = json[index].label
    badgeDesc = json[index].description
    badgeSolution = json[index].solution
    badgeIcon = json[index].badgeIcon
    foundBadge = true
  }
}

if (!foundBadge) {
  badgeName = json[0].label
  badgeDesc = json[0].description
  badgeSolution = json[0].solution
  badgeIcon = json[0].badgeIcon
}
</script>

<style>

</style>