<template lang="html">
  <div class="container ">
    <div class="row">
      <div class="col-sm-4 " v-for="project in Projects" :key="project.id">
        <ProjectCard :category="project.category" :title="project.title" :tags="project.tags" :description="project.description" :modal_content="project.modal_content" :modal_id="project.modal_id"/>
      </div>
    </div>
  </div>
</template>

<script>
import ProjectCard from './ProjectCard.vue'
export default {
  components: {
    ProjectCard
  },
  data() {
    return {
      modal_id: 0,
      Projects : [
        {
          category: 'Konzol alkalmazás',
          image_path: '../imagepath.png',
          title: 'Valutaátváltó',
          tags: ['Python'],
          description: 'Egy terminál alapú valutaátváltó alkalmazás. A program angol és magyar nyelveken is használható, részletes dokumentáció készült hozzá, és a legfontosabb modulok tesztelve lettek.',
          modal_id: 'first',
          modal_content: 'modal content text'
        },
        {
          category: 'Konzol alkalmazás',
          image_path: '../imagepath.png',
          title: 'Órarend elemzés',
          tags: ['Python'],
          description: 'A szakkollégiumban is hétköznapi probléma a tagok idejének összeegyeztetése, ráadásul mindenki beosztása félévenként változik. Ezért megpróbáltam egy megoldást nyújtani a problémára, amivel az egyeztetést felgyorsíthatjuk.',
          modal_id: 'second',
          modal_content: 'second modal content text'
        },
        {
          category: 'Konzol alkalmazás',
          image_path: '../imagepath.png',
          title: 'Számrendszerek kezelése ',
          tags: ['Python'],
          description: 'Sokszor nagy segítséget nyújt, ha nem manuálisan kell a számrendszerek közötti átváltást elvégezni. Erre az alapvető egyszerű feladatra készült ez a Python script, hogy meggyorsítsa az ehhez kapcsolódó feladatok megoldását. ',
          modal_id: 'third',
          modal_content: 'third modal content text'
        },
        {
          category: 'Backend ',
          image_path: '../imagepath.png',
          title: 'Kék Mancs szervezet ',
          tags: ['PHP', 'Codeigniter 3'],
          description: 'Egy fiktív szervezet számára készült nyilvántartó web alkalmazás. ',
          modal_id: 'fourth',
          modal_content: 'fourth modal content text'
        }
      ]
    }
  }
}
</script>

<style lang="css" scoped>
</style>
