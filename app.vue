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
import bbBadges from './public/assets/list/bb.json';
import dbBadges from './public/assets/list/db.json';
import generalBadges from './public/assets/list/general.json';
import hitwBadges from './public/assets/list/hitw.json';
import pkwBadges from './public/assets/list/pkw.json';
import rsrBadges from './public/assets/list/rsr.json';
import sbBadges from './public/assets/list/sb.json';
import tgttosBadges from './public/assets/list/tgttos.json';

var searchOpen = ref(false)
const commandPaletteRef = ref()

const groups = computed(() =>
  [
    {
      key: 'general',
      label: 'General Badges',
      commands: generalBadges
    },
    {
      key: 'bb',
      label: 'Battle Box Badges',
      commands: bbBadges
    },
    {
      key: 'db',
      label: 'Dynaball Badges',
      commands: dbBadges
    },
    {
      key: 'hitw',
      label: 'Hole in the Wall Badges',
      commands: hitwBadges
    },
    {
      key: 'pkw',
      label: 'Parkour Warrior Badges',
      commands: pkwBadges
    },
    {
      key: 'rsr',
      label: 'Rocket Spleef Rush Badges',
      commands: rsrBadges
    },
    {
      key: 'sb',
      label: 'Sky Battle Badges',
      commands: sbBadges
    },
    {
      key: 'tgttos',
      label: 'To Get to the Other Side Badges',
      commands: tgttosBadges
    },
  ].filter(Boolean))

function onSelect (option) {
  window.open(option.link, "_self")
}
</script>
