<template lang="html">
  <a :href="src" target="_blank">
    <h2 class="p-2 text-info" :class="icon_type"></h2>
  </a>

</template>

<script>
export default {
  props: {
    icon_type: String,
    src: String
  }
}
</script>

<style lang="css" scoped>
</style>
