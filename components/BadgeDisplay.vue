<template>
  <div class="hstack">
    <img :src="icon" alt="" width="96">
    <div class="ml-4">
      <h1 class="text-2xl">{{ name }}</h1>
      <div class="hstack">
        <p class="mr-1">{{ reward }}</p>
        <img v-show="isSkill" src="/assets/badges/icons/trophy/red.png" alt="">
        <img v-show="!isSkill" src="/assets/badges/icons/trophy/silver.png" alt="">
        
      </div>
      <p>{{ solution }}</p>
      <p v-show="!obtainable">Unobtainable</p>
    </div>
  </div>
</template>

<script>
export default defineComponent({
  props: {
    name: {
      type: String,
      default: () => "The Badge is missing a name. Open an issue on the GitHub repository of IslandBadges.",
    },
    icon: {
      type: String,
      default: () => "/assets/badges/icons/missing.png",
    },
    solution: {
      type: String,
      default: () => "The Badge is missing a solution. Open an issue on the GitHub repository of IslandBadges.",
    },
    reward: {
      type: Number,
      default: () => 0
    },
    isSkill: {
      type: Boolean,
      default: () => true
    },
    obtainable: {
      type: Boolean,
      default: () => true
    }
  }
})
</script>

<style>
.hstack {
  display: flex;
  align-items: center;
  justify-content: start;
}
</style>