<template lang="html">
  <div class="row">
    <div class="col-md-3">
    <PersonalCard/>
    </div>
    <div class="col">
    <Introduction/>
    </div>
  </div>
</template>

<script>
import Introduction from './Introduction.vue'
import PersonalCard from './PersonalCard.vue'

export default {
  components: {
    Introduction,
    PersonalCard
  }
}
</script>

<style lang="css" scoped>
</style>
