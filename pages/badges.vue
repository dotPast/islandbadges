<template>
  <div>
    <h1 class="text-4xl mb-4">General</h1>
    <IconBadgeDisplay v-for="badge in generalBadges" :name="badge.label" :icon="badge.badgeIcon" :link="badge.link"/>
  </div>
  <div>
    <h1 class="text-4xl mb-4">Battle Box</h1>
    <IconBadgeDisplay v-for="badge in bbBadges" :name="badge.label" :icon="badge.badgeIcon" :link="badge.link"/>
  </div>
  <div>
    <h1 class="text-4xl mb-4">Dynaball</h1>
    <IconBadgeDisplay v-for="badge in dbBadges" :name="badge.label" :icon="badge.badgeIcon" :link="badge.link"/>
  </div>
  <div>
    <h1 class="text-4xl mb-4">Hole in the Wall</h1>
    <IconBadgeDisplay v-for="badge in hitwBadges" :name="badge.label" :icon="badge.badgeIcon" :link="badge.link"/>
  </div>
  <div>
    <h1 class="text-4xl mb-4">Parkour Warrior</h1>
    <IconBadgeDisplay v-for="badge in pkwBadges" :name="badge.label" :icon="badge.badgeIcon" :link="badge.link"/>
  </div>
  <div>
    <h1 class="text-4xl mb-4">Rocket Spleef Rush</h1>
    <IconBadgeDisplay v-for="badge in rsrBadges" :name="badge.label" :icon="badge.badgeIcon" :link="badge.link"/>
  </div>
  <div>
    <h1 class="text-4xl mb-4">Sky Battle</h1>
    <IconBadgeDisplay v-for="badge in sbBadges" :name="badge.label" :icon="badge.badgeIcon" :link="badge.link"/>
  </div>
  <div>
    <h1 class="text-4xl mb-4">To Get to the Other Side</h1>
    <IconBadgeDisplay v-for="badge in tgttosBadges" :name="badge.label" :icon="badge.badgeIcon" :link="badge.link"/>
  </div>
</template>

<script lang="ts" setup>
import bbBadges from '../public/assets/list/bb.json';
import dbBadges from '../public/assets/list/db.json';
import generalBadges from '../public/assets/list/general.json';
import hitwBadges from '../public/assets/list/hitw.json';
import pkwBadges from '../public/assets/list/pkw.json';
import rsrBadges from '../public/assets/list/rsr.json';
import sbBadges from '../public/assets/list/sb.json';
import tgttosBadges from '../public/assets/list/tgttos.json';
</script>

<style></style>