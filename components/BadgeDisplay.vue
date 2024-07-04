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
      default: () => "Missing Badge",
    },
    icon: {
      type: String,
      default: () => "/assets/badges/missing.png",
    },
    description: {
      type: String,
      default: () => "?",
    },
    solution: {
      type: String,
      default: () => "?",
    }
  }
})
</script>

<style>

</style>