<template lang="html">
  <div class="info_block">
      <h6 class="text-info">{{type}}:</h6> <p class="text-secondary">{{data}}</p>
  </div>

</template>

<script>
export default {
  props: {
    type : String,
    data : String
  }
}
</script>

<style lang="css" scoped>
h6 {
  display: inline-block;
}
p {
  display: inline-block;
}

.info_block {
  width: 340px;
}
</style>
