<template>
<Navbar/>
  <div class="container mt-3">
    <BlockTitle title_text="Elérhetőségek"/>
    <BasicInfomration/>
    <BlockTitle title_text="Rólam"/>
    <IntroductionBlock/>
    <BlockTitle title_text="Ismereteim"/>
  </div>
</template>

<script>
import BasicInfomration from './components/BasicInfomration.vue'
import BlockTitle from './components/BlockTitle.vue'
import IntroductionBlock from './components/IntroductionBlock.vue'
import Navbar from './components/Navbar.vue'


export default {
  provide: {
    language: 'hungarian'
  },
  name: 'App',
  components: {
    BasicInfomration,
    BlockTitle,
    IntroductionBlock,
    Navbar
  }
}
</script>

<style>
#appl {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
