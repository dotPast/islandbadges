<template>
  <UModal v-model="searchOpen">
    <UCommandPalette ref="commandPaletteRef" :groups="groups" :autoselect="false" @update:model-value="onSelect" />
  </UModal>
  <UContainer>
    <UCard class="mt-10">
      <template #header>
        <div class="flex justify-between">
          <UButtonGroup>
            <UButton label="All Badges" icon="tabler:medal" to="/badges"/>
            <UButton label="Search" icon="tabler:search" @click="searchOpen = true"/>
          </UButtonGroup>
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
  window.open(option.link, "_self")
}
</script>
