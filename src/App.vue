<template>
  <Navbar :param="param" @change="update_state" />
  <div v-if="page_state == 0" class="mt-3">
    <BlockTitle title_text="Elérhetőségek"/>
    <BasicInformation/>
    <BlockTitle title_text="Rólam"/>
    <IntroductionBlock/>
    <BlockTitle title_text="Ismereteim"/>
    <Stack/>
  </div>
  <div v-else-if="page_state == 1" class="container mt-3">
    <BlockTitle title_text="Önéletrajz"/>
    <div class="container bg-white shadow-sm rounded mt-3 border p-1">
      <p class="m-3 text-secondary">Az önéletrajzom PDF formátumban <a href="#">elérhető itt.</a></p>
    </div>

  <div class="container rounded bg-white p-2 my-3 border shadow-sm">
      <Cv />
  </div>

  </div>
  <div v-else-if="page_state == 2" class="container mt-3">
    <BlockTitle title_text="Projektek"/>
  </div>
  <div v-else-if="page_state == 3" class="container mt-3">
    <BlockTitle title_text="Hobbi"/>
  </div>
  <div v-else class="container mt-3">
    <BlockTitle title_text="ERROR 404"/>
  </div>
</template>

<script>
import BasicInformation from './components/BasicInformation.vue'
import BlockTitle from './components/BlockTitle.vue'
import IntroductionBlock from './components/IntroductionBlock.vue'
import Navbar from './components/Navbar.vue'
import Stack from './components/Stack.vue'
import Cv from './components/Cv.vue'


export default {
  provide: {
    language: 'english'
  },
  name: 'App',
  components: {
    BasicInformation,
    BlockTitle,
    IntroductionBlock,
    Navbar,
    Stack,
    Cv
  },
  data() {
    return {
      page_state: 0,
    }
  },
  methods: {
    update_state(e) {
      this.page_state = e
    }
  }
}
</script>

<style>
#appl {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
