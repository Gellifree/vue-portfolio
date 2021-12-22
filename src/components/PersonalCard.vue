<template lang="html">
  <div class="card my-3">
    <img class="card-img-top" src="../assets/logo.png" alt="Card image">
    <div class="card-body text-center">
      <h4 class="card-title"> {{ name }} </h4>
      <p class="card-text text-secondary"> {{ studies }} </p>
    </div>


  </div>
</template>

<script>
export default {
  data() {
    return {
      name: 'Kovács Norbert',
      studies: 'egyetemi hallgató'
    }
  }
}
</script>

<style lang="css" scoped>
</style>
