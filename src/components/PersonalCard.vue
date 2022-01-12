<template lang="html">
  <div class="card my-3 shadow-sm">
    <img class="card-img-top" src="../assets/me_bw.jpg" alt="Card image">
    <div class="card-body text-center" v-if="language['value'] == 'EN'">
      <h4 class="card-title"> {{ hungarian_lang.name }} </h4>
      <p class="card-text text-secondary"> {{ hungarian_lang.studies }} </p>
      <SocialIcon icon_type="fab fa-github" src="https://github.com/Gellifree"/>
      <SocialIcon icon_type="fab fa-hackerrank" src="https://hackerrank.com/kovacs1"/>
      <SocialIcon icon_type="fab fa-facebook-square" src="https://facebook.com/kovacs.norbert.fb"/>
      <SocialIcon icon_type="fas fa-code" src="https://profile.codersrank.io/user/gellifree"/>
    </div>
    <div class="card-body text-center" v-else>
      <h4 class="card-title"> {{ english_lang.name }} </h4>
      <p class="card-text text-secondary"> {{ english_lang.studies }} </p>
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
      }
    }
  }
}
</script>

<style lang="css" scoped>
</style>
