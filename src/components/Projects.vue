<template lang="html">
  <div class="container ">
    <div class="row" v-if="language['value'] == 'EN'">
      <div class="col-sm-4 " v-for="project in hungarian_lang.Projects" :key="project.id">
        <ProjectCard :category="project.category" :title="project.title" :tags="project.tags" :description="project.description" :modal_content="project.modal_content" :modal_id="project.modal_id"/>
      </div>
    </div>
    <div class="row" v-else>
      <div class="col-sm-4 " v-for="project in english_lang.Projects" :key="project.id">
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
  inject: ['language'],
  data() {
    return {
      hungarian_lang: {
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
      },
      english_lang: {
        Projects : [
          {
            category: 'Console application',
            image_path: '../imagepath.png',
            title: 'Currency Converter',
            tags: ['Python'],
            description: 'A terminal-based currency exchange application. The program can be used in both English and Hungarian, detailed documentation has been prepared, and the most important modules have been tested.',
            modal_id: 'first',
            modal_content: 'modal content text'
          },
          {
            category: 'Console application',
            image_path: '../imagepath.png',
            title: 'Timetable management',
            tags: ['Python'],
            description: "Reconciling the time of the members is also a common problem in the vocational college, and everyone's schedule changes every six months. That is why I have tried to provide a solution to the problem so that we can speed up the conciliation.",
            modal_id: 'second',
            modal_content: 'second modal content text'
          },
          {
            category: 'Console application',
            image_path: '../imagepath.png',
            title: 'Management of number systems ',
            tags: ['Python'],
            description: 'It is often very helpful not to have to manually calculate between number systems. This Python script is designed for this basic simple task to speed up the tasks involved.',
            modal_id: 'third',
            modal_content: 'third modal content text'
          },
          {
            category: 'Backend ',
            image_path: '../imagepath.png',
            title: 'Blue Paw',
            tags: ['PHP', 'Codeigniter 3'],
            description: 'A registry web application designed for a fictitious organization.',
            modal_id: 'fourth',
            modal_content: 'fourth modal content text'
          }
        ]
      },
    }
  }
}
</script>

<style lang="css" scoped>
</style>
