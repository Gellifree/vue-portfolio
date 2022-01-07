<template lang="html">
  <div class="row block rounded mx-3">
    <div class="col- icon  rounded bg-white text-center">
    </div>
    <div class="col title-box border p-3 container rounded">
      <h6 class="m-0 text-info rounded">{{title}}</h6>
      <p class="text-secondary">{{date}}</p>
      <span class="text-secondary" v-for="data in datas" :key="data.id">
        <p class="my-0">{{data}}</p>
      </span>
    </div>
  </div>
</template>

<script>
export default {
  props : {
    title: String,
    date: String,
    datas: Array
  }
}
</script>

<style lang="css" scoped>
.icon {
  width: 50px;
  height: 50px;
}

p {
  font-size: 13px;
}
</style>
