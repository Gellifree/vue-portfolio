<template lang="html">
  <div class="row block rounded mx-3">
    <div class="col- icon  rounded bg-white text-center">
    </div>
    <div class="col title-box border p-3 container rounded">
      <h6 class="m-0 text-secondary rounded">{{title}}</h6>
      <p>{{date}}</p>
      <p>{{data}}</p>
    </div>
  </div>
</template>

<script>
export default {
  props : {
    title: String,
    date: String,
    data: String
  }
}
</script>

<style lang="css" scoped>
.icon {
  width: 50px;
  height: 50px;
}
</style>
