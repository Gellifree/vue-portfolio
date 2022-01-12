<template >
  <div class="container my-3">
    <div class="row bg-white border py-3 shadow-sm" v-if="language['value'] == 'EN'">
      <div class="col" v-for="(value, key) in hungarian_lang.informations" :key="key">
          <BasicInformationBlock :type="key" :data="value"/>
      </div>
    </div>
    <div class="row bg-white border py-3 shadow-sm" v-else>
      <div class="col" v-for="(value, key) in english_lang.informations" :key="key">
          <BasicInformationBlock :type="key" :data="value"/>
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
    BasicInformationBlock,
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
      }
    }
  },
}
</script>

<style scoped>
</style>
