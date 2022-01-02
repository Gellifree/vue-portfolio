<template lang="html">
  <div class="stack_block">
    <h6 class="text-info"> {{ stack_title }} </h6>
    <p class="text-secondary"> {{ stack_description }} </p>
  </div>

</template>

<script>
export default {
  props: {
    stack_title: String,
    stack_description: String
  }
}
</script>

<style lang="css" scoped>
p {
  font-size: 11px;
}

.stack_block{
  width: 350px;
  
}
</style>
