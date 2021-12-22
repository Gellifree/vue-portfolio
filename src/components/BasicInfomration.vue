<template>
  <div class="container border">
    <ul>
      <li v-for="(value, key) in informations" :key="key">
        {{ key }} : {{ value }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      informations: {
        'Teljes név': 'Kovács Norbert',
        'Születési dátum': '1995.02.24',
        'Tanulmányok': 'Programtervező Informatika',
        'Telefon': '+36 70 517 09 49',
        'E-mail': 'mfw.kovacs.norbert@gmail.com',
        'Lakhely': 'Eger'
      }
    }
  }
}
</script>

<style scoped>
</style>
