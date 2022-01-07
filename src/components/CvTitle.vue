<template lang="html">
  <div class="row m-3">
    <div class="col- icon border rounded bg-info text-center">
      <h6 :class="icon_type" class="text-white my-3 mx-auto"></h6>
    </div>
    <div class="col title-box border p-3 container rounded">
      <h6 class="m-0 text-secondary rounded">{{title}}</h6>
    </div>

  </div>
</template>

<script>
export default {
  props : {
    icon_type: String,
    title: String
  }
}
</script>

<style lang="css" scoped>
.icon {
  width: 50px;
  height: 50px;
}
.icon-right {
  width: 55px;
  height: 50px;
}

.title-box {
  height: 50px;
}
</style>
