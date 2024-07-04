<template>
  <div>
    <div v-for="data in badges">
      <BadgeDisplay :name="data.label" :icon="data.badgeIcon" :description="data.description" :solution="data.solution" />
    </div>
    
  </div>
</template>

<script lang="ts" setup>
import badges from '../public/assets/badges.json';
</script>

<style></style>