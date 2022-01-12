<template>
  <Navbar @change="update_state" @language_change="change_root_language"/>
  <div v-if="page_state == 0" class="mt-3">
    <div v-if="language['value'] == 'EN'">
      <BlockTitle title_text="Elérhetőségek"/>
      <BasicInformation/>
      <BlockTitle title_text="Rólam"/>
      <IntroductionBlock/>
      <BlockTitle title_text="Ismereteim"/>
      <Stack/>
    </div>
    <div class="" v-else>
      <BlockTitle title_text="Contact"/>
      <BasicInformation/>
      <BlockTitle title_text="About me"/>
      <IntroductionBlock/>
      <BlockTitle title_text="Knowledge"/>
      <Stack/>
    </div>

  </div>
  <div v-else-if="page_state == 1" class="container mt-3">
    <div v-if="language['value'] == 'EN'">
      <BlockTitle title_text="Önéletrajz"/>
      <div class="container bg-white shadow-sm rounded mt-3 border p-1">
        <p class="m-3 text-secondary">Az önéletrajzom PDF formátumban <a href="#">elérhető itt.</a></p>
      </div>

      <div class="container rounded bg-white p-2 my-3 border shadow-sm">
        <Cv />
      </div>
    </div>
    <div v-else>
      <BlockTitle title_text="CV"/>
      <div class="container bg-white shadow-sm rounded mt-3 border p-1">
        <p class="m-3 text-secondary">My CV can be downloaded <a href="#">here.</a></p>
      </div>
      <div class="container rounded bg-white p-2 my-3 border shadow-sm">
        <Cv />
      </div>
    </div>


  </div>
  <div v-else-if="page_state == 2" class="container mt-3">
    <div v-if="language['value'] == 'EN'">
      <BlockTitle title_text="Projektek"/>
      <div class="container rounded bg-white p-3 my-3 border shadow-sm">
        <h6 class="text-secondary">Munkáim</h6>
        <p class="text-secondary">Itt találhatóak meg a kiemelt projektjeim. Megpróbálok mélyebb
          betekintést nyújtani a folyamatokba, és a projektek nehézségeibe,
          tapasztalataiba is. A projektek többsége egyetemi projekt, viszont
          fontos hogy az egyetemi projektjeim céltudatosan kerültek elkészítésére,
          és sok esetben az egyetemi feladat letudtával, a projektek továbbfejlesztésre kerültek saját felhasználásra.

        </p>
      </div>
    </div>
    <div v-else>
      <BlockTitle title_text="Projetcs"/>
      <div class="container rounded bg-white p-3 my-3 border shadow-sm">
        <h6 class="text-secondary">Works</h6>
        <p class="text-secondary">Here are my featured projects. I'll try deeper
          provide insight into processes and project difficulties,
          experience. Most of the projects are university projects, however
          it is important that my university projects have been purposefully prepared,
          and in many cases, with the completion of the university assignment, the projects were further developed for my own use.
        </p>
      </div>
    </div>

    <Projects />
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
import Projects from './components/Projects.vue'

export default {
  provide() {
    return {
      language: this.language
    };
  },
  name: 'App',
  components: {
    BasicInformation,
    BlockTitle,
    IntroductionBlock,
    Navbar,
    Stack,
    Cv,
    Projects
  },
  data() {
    return {
      page_state: 0,
      language: {
        value: 'HU'
      }
    }
  },
  methods: {
    update_state(e) {
      this.page_state = e
    },
    change_root_language() {
      this.set_language()

    },
    set_language() {
      if(this.language['value'] == "HU") {
        this.language['value'] = "EN"
      } else {
        this.language['value'] = 'HU'
      }
      console.log('the language is set to: ', this.language['value'])

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

p {
  font-size: 13px;
}
</style>
