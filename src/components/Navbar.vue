<template lang="html">
  <nav class="navbar navbar-expand-md bg-dark navbar-dark px-3">
 <!-- Brand -->
 <a class="navbar-brand" href="#" @click.prevent="set_page_state(0)">Kovács Norbert</a>

 <!-- Toggler/collapsibe Button -->
 <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#collapsibleNavbar">
   <span class="navbar-toggler-icon"></span>
 </button>

 <!-- Navbar links -->
 <div class="collapse navbar-collapse" id="collapsibleNavbar">
   <ul class="navbar-nav">
     <li class="nav-item">
       <a class="nav-link" href="#" @click.prevent="set_page_state(1)">Önéletrajz</a>
     </li>
     <li class="nav-item">
       <a class="nav-link" href="#" @click.prevent="set_page_state(2)">Projektek</a>
     </li>
     <li class="nav-item">
       <a class="nav-link" href="#" @click.prevent="set_page_state(3)">Hobbi</a>
     </li>
   </ul>
   <span class="text-white mr-3" style="display:inline-block;">Change language to: </span>
   <a href="#" @click="set_language" class="mx-2" style="display: inline-block;">{{language['value']}}</a>
 </div>

</nav>
</template>

<script>
export default {
  inject: ['language'],
  methods: {
    set_page_state(param) {
      this.$emit('change', param)
    },
    set_language() {
      this.$emit('language_change')
    }
  },
  data() {
    return {
      hungarian_lang: {

      },
      english_lang: {

      }
    }
  }
}
</script>

<style lang="css" scoped>
</style>
