<template>
  <IconBadgeDisplay :name="data.label" :icon="data.badgeIcon" :link="data.link" v-for="data in badges"/>
</template>

<script lang="ts" setup>
import badges from '../public/assets/badges.json';
</script>

<style></style>