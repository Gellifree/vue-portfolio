<template lang="html">
  <div class="card m-3 shadow-sm border" style="width: 375px;">
    <div class="card-header bg-dark text-white"> {{category}} </div>
    <img class="card-img-top" src="../assets/ProjectImages/binary.png"/>
    <div class="card-body">
      <h6 class="card-title text-secondary">{{title}}</h6>
      <span class="badge rounded-pill bg-info text-white mx-1" v-for="tag in tags" :key="tag.id">{{tag}}</span>
      <p class="card-text mt-2 text-secondary">{{description}}</p>

      <button class="btn btn-info text-white" data-bs-toggle="modal" :data-bs-target="'#' + modal_id" v-if="language['value'] == 'EN'">Részletek</button>
      <button class="btn btn-info text-white" data-bs-toggle="modal" :data-bs-target="'#' + modal_id" v-else>Details</button>

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
          <h6> {{ modal_content.modal_title }}</h6>
          <p class="text-secondary" v-for="paragraph in modal_content.paragraps" :key="paragraph.id">{{paragraph}}</p>

          <div id="carouselExampleCaptions" class="carousel slide" data-bs-ride="carousel">
            <div class="carousel-indicators">
              <button type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide-to="0" class="active" aria-current="true" aria-label="Slide 1"></button>
              <button type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide-to="1" aria-label="Slide 2"></button>
              <button type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide-to="2" aria-label="Slide 3"></button>
            </div>
            <div class="carousel-inner">
              <div class="carousel-item active">
                <img src="../assets/Detailes/currency_screenshot_exchange.png" class="d-block w-100" alt="...">
              </div>
              <div class="carousel-item">
                <img src="../assets/Detailes/currency_screenshot_list.png" class="d-block w-100" alt="...">
              </div>
            </div>
            <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide="prev">
              <span class="carousel-control-prev-icon" aria-hidden="true"></span>
              <span class="visually-hidden">Previous</span>
            </button>
            <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide="next">
              <span class="carousel-control-next-icon" aria-hidden="true"></span>
              <span class="visually-hidden">Next</span>
            </button>
          </div>


          <button type="button" name="button" class="btn btn-danger m-2 float-end">Bezár</button>
          <button type="button" name="button" class="btn btn-outline-info m-2 float-end">Github</button>

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
    modal_content: Object
  },
  inject: ['language']
}
</script>

<style lang="css" scoped>
</style>
