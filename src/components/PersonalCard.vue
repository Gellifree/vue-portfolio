<template lang="html">
  <div class="card my-3 shadow-sm">
    <img class="card-img-top" src="../assets/me_bw.jpg" alt="Card image">
    <div class="card-body text-center">
      <h4 class="card-title"> {{ final_data.name }} </h4>
      <p class="card-text text-secondary"> {{ final_data.studies }} </p>
      <SocialIcon icon_type="fab fa-github" src="https://github.com/Gellifree"/>
      <SocialIcon icon_type="fab fa-hackerrank" src="https://hackerrank.com/kovacs1"/>
      <SocialIcon icon_type="fab fa-facebook-square" src="https://facebook.com/kovacs.norbert.fb"/>
      <SocialIcon icon_type="fas fa-code" src="https://profile.codersrank.io/user/gellifree"/>
    </div>


  </div>
</template>

<script>
import SocialIcon from './SocialIcon.vue'

export default {
  name: 'Personal Card Component',
  components: {
    SocialIcon
  },
  inject: ['language'],
  data() {
    return {
      hungarian_lang: {
        name: 'Kovács Norbert',
        studies: 'egyetemi hallgató'
      },
      english_lang: {
        name: 'Norbert Kovács',
        studies: 'university student'
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

<style lang="css" scoped>
</style>
