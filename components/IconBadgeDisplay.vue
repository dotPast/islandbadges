<template>
  <a :href="link" class="mr-2">
    <UTooltip :text="name">
      <img :src="icon" width="96">
    </UTooltip>
  </a>
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
      default: () => "/assets/badges/missing.png",
    },
    link: {
      type: String,
      default: () => "/badge/missing"
    }
  }
})
</script>

<style></style>