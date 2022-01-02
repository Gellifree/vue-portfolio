<template lang="html">
  <div class="card my-3">
    <img class="card-img-top" src="../assets/logo.png" alt="Card image">
    <div class="card-body text-center">
      <h4 class="card-title"> {{ final_data.name }} </h4>
      <p class="card-text text-secondary"> {{ final_data.studies }} </p>
    </div>


  </div>
</template>

<script>
export default {
  name: 'Personal Card Component',
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
