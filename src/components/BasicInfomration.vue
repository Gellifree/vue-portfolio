<template>
  <div class="container my-3">
   <!--  <ul class="list-group">
      <li v-for="(value, key) in informations" :key="key" class="list-group-item">
       <b class="text-info">{{ key }}</b> : {{ value }}
      </li>
    </ul>
-->
    <div class="row bg-white border py-3 shadow-sm">
      <div class="col col-l" v-for="(value, key) in informations" :key="key">
        <h6 class="text-info medium-text">{{ key }}</h6> <span class="small-text text-secondary">{{ value }}</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      informations: {
        'Teljes név': 'Kovács Norbert',
        'Tanulmányok': 'Programtervező Informatika',
        'Telefon': '+36 70 517 09 49',
        'E-mail': 'mfw.kovacs.norbert@gmail.com',
      }
    }
  }
}
</script>

<style scoped>
</style>
