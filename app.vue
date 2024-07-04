<template>
  <UModal v-model="searchOpen">
    <UCommandPalette ref="commandPaletteRef" :groups="groups" :autoselect="false" @update:model-value="onSelect" />
  </UModal>
  <UContainer>
    <UCard class="mt-10">
      <template #header>
        <div class="flex justify-between">
          <h1>Welcome to Nuxt UI Starter</h1>
          <ColorScheme>
            <USelect v-model="$colorMode.preference" :options="['system', 'light', 'dark']" />
          </ColorScheme>
        </div>
      </template>
      <NuxtPage />
    </UCard>
  </UContainer>
</template>

<script setup lang="ts">
import badges from './public/assets/badges.json';
badges.shift()

var searchOpen = ref(false)
const commandPaletteRef = ref()

const groups = computed(() =>
  [
    {
      key: 'badges',
      commands: badges
    }
  ].filter(Boolean))

function onSelect (option) {
  window.open(option.link)
}</script>
