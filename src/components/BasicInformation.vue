<template>
  <div class="container my-3">
   <!--  <ul class="list-group">
      <li v-for="(value, key) in informations" :key="key" class="list-group-item">
       <b class="text-info">{{ key }}</b> : {{ value }}
      </li>
    </ul>
-->
    <div class="row bg-white border py-3 shadow-sm">
      <div class="col" v-for="(value, key) in final_data.informations" :key="key">
        <!-- <h6 class="text-info medium-text">{{ key }}</h6> <span class="small-text text-secondary">{{ value }}</span> -->
          <BasicInformationBlock :type="key" :data="value" />
      </div>
    </div>
  </div>
</template>

<script>
import BasicInformationBlock from './BasicInformationBlock.vue'

export default {
  name: 'Basic Information Component',
  inject: ['language'],
  components: {
    BasicInformationBlock
  },
  data() {
    return {
      hungarian_lang: {
        informations: {
          'Teljes név' : 'Kovács Norbert',
          'Születési dátum' : '1995. február 24.',
          'Tanulmányok': 'Programtervező Informatika',
          'Telefon': '+36 70 517 09 49',
          'E-mail': 'mfw.kovacs.norbert@gmail.com',
          'Lakhely': 'Eger'
        }
      },
      english_lang: {
        informations: {
          'Full name': 'Norbert Kovács',
          'Birthday' : '1995. február 24.',
          'Studies': 'Programming',
          'Phone number': '+36 70 517 09 49',
          'E-mail': 'mfw.kovacs.norbert@gmail.com',
          'Place': 'Eger'
        }
      },
      final_data: {
      }
    }
  },
  methods: {
    set_language() {
      if(this.language == "hungarian") {
        this.final_data = this.hungarian_lang
      } else if(this.language == "english") {
        this.final_data = this.english_lang
      }
    }
  },
  beforeMount() {
    this.set_language()
  }
}
</script>

<style scoped>
</style>
