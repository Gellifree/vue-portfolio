<template lang="html">
  <div class="info_block">
      <h6 class="text-info">{{type}}:</h6> <p class="text-secondary">{{data}}</p>
  </div>

</template>

<script>
export default {
  props: {
    type : String,
    data : String
  },
  methods: {
    set_language() {
      console.log('set_language called from Block')
      if(this.language['value'] == "hungarian") {
        console.log('The language is set to hungarian')
        this.final_data = this.hungarian_lang
      } else {
        console.log('The language is set to english')
        this.final_data = this.english_lang
      }
    }
  },
}
</script>

<style lang="css" scoped>
h6 {
  display: inline-block;
}
p {
  display: inline-block;
}

.info_block {
  width: 340px;
}
</style>
