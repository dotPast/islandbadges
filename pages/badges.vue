<template>
  <div>
    <div v-for="data in json">{{data.name}}</div>
  </div>
</template>

<script lang="ts" setup>
import json from '/assets/badges.json';
</script>

<style></style>