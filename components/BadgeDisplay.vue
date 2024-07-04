<template>
  <div>
    {{ name }} - {{ description }} - {{ solution }} - {{ icon }}
  </div>
</template>

<script>
export default defineComponent({
  props: {
    name: {
      type: String,
      default: () => "The Badge is missing a name. Open an issue on GitHub repository of IslandBadges.",
    },
    icon: {
      type: String,
      default: () => "/assets/badges/missing.png",
    },
    description: {
      type: String,
      default: () => "The badge is missing a description. Open an issue on GitHub repository of IslandBadges.",
    },
    solution: {
      type: String,
      default: () => "The badge is missing a solution. Open an issue on GitHub repository of IslandBadges.",
    }
  }
})
</script>

<style>

</style>