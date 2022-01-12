<template lang="html">
  <div class="card m-3 shadow-sm border" style="width: 375px;">
    <div class="card-header bg-dark text-white"> {{category}} </div>
    <img class="card-img-top" src="../assets/ProjectImages/binary.png"/>
    <div class="card-body">
      <h6 class="card-title text-secondary">{{title}}</h6>
      <span class="badge rounded-pill bg-info text-white mx-1" v-for="tag in tags" :key="tag.id">{{tag}}</span>
      <p class="card-text mt-2 text-secondary">{{description}}</p>

      <button class="btn btn-info text-white" data-toggle="modal" :data-target="'#' + modal_id" v-if="language['value'] == 'EN'">Részletek</button>
      <button class="btn btn-info text-white" data-toggle="modal" :data-target="'#' + modal_id" v-else>Details</button>

      <a class="btn btn-outline-info float-end " href="#">Github</a>
    </div>
  </div>

  <div class="modal fade mt-5 rounded" :id="modal_id">
    <div class="modal-dialog modal-lg">
      <div class="modal-content">
        <div class="modal-header bg-dark text-white">
          <h6 class="modal-title">{{title}}</h6>
        </div>
        <div class="modal-body">
          <p>{{modal_content}}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    category: String,
    image_path: String,
    title: String,
    tags: Array,
    description: String,
    modal_id: String,
    modal_content: String
  },
  inject: ['language']
}
</script>

<style lang="css" scoped>
</style>
