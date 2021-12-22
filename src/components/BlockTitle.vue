<template lang="html">
  <div class="container bg-dark rounded shadow-sm">
    <h6 class="text-white b-2 py-2"> {{ title_text }} </h6>
  </div>
</template>

<script>
export default {
  props: {
    title_text: String
  }
}
</script>

<style lang="css" scoped>
</style>
