<template>
  <div>
    <div v-for="data in json"><BadgeDisplay :name="data.name" :icon="data.icon" :description="data.description" :solution="data.solution"/></div>
  </div>
</template>

<script lang="ts" setup>
import json from '../public/assets/badges.json';
</script>

<style></style>