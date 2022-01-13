<template lang="html">
  <nav class="navbar navbar-expand-md bg-dark navbar-dark px-3">
 <!-- Brand -->
 <a class="navbar-brand" href="#" @click.prevent="set_page_state(0)" v-if="language['value'] == 'EN'">{{hungarian_lang['name_logo']}}</a>
 <a class="navbar-brand" href="#" @click.prevent="set_page_state(0)" v-else>{{english_lang['name_logo']}}</a>

 <!-- Toggler/collapsibe Button -->
 <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#collapsibleNavbar">
   <span class="navbar-toggler-icon"></span>
 </button>

 <!-- Navbar links -->
 <div class="collapse navbar-collapse" id="collapsibleNavbar">
   <ul class="navbar-nav" v-if="language['value'] == 'EN'">
     <li class="nav-item">
       <a class="nav-link" href="#" @click.prevent="set_page_state(1)"> {{hungarian_lang['cv']}}</a>
     </li>
     <li class="nav-item">
       <a class="nav-link" href="#" @click.prevent="set_page_state(2)">{{hungarian_lang['projects']}}</a>
     </li>
     <li class="nav-item">
       <a class="nav-link" href="#" @click.prevent="set_page_state(3)">{{hungarian_lang['hobbies']}}</a>
     </li>
   </ul>
   <ul class="navbar-nav" v-else>
     <li class="nav-item">
       <a class="nav-link" href="#" @click.prevent="set_page_state(1)">{{english_lang['cv']}}</a>
     </li>
     <li class="nav-item">
       <a class="nav-link" href="#" @click.prevent="set_page_state(2)">{{english_lang['projects']}}</a>
     </li>
     <li class="nav-item">
       <a class="nav-link" href="#" @click.prevent="set_page_state(3)">{{english_lang['hobbies']}}</a>
     </li>
   </ul>

   <!--<span class="text-white ms-auto mb-2 mb-lg-0"  v-if="language['value'] == 'EN'"> {{ hungarian_lang.change_lang_title}} </span>
   <span class="text-white ms-auto mb-2 mb-lg-0"  v-else> {{ english_lang.change_lang_title}} </span> -->
   <a @click.prevent="set_language" class="mx-2 btn btn-info text-white ms-auto mb-2 mb-lg-0" style="display: inline-block;">{{language['value']}}</a>
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
        name_logo: 'Kovács Norbert',
        cv: 'Önéletrajz',
        projects: 'Projektek',
        hobbies: 'Hobbi',
        change_lang_title: 'Nyelv megváltoztatása: '
      },
      english_lang: {
        name_logo: 'Norbert Kovács',
        cv: 'CV',
        projects: 'Projects',
        hobbies: 'Hobby',
        change_lang_title: 'Change language to: '
      }
    }
  }
}
</script>

<style lang="css" scoped>
</style>
