<template>
<Navbar/>
  <div class="container mt-3">
    <BlockTitle title_text="Elérhetőségek"/>
    <BasicInformation/>
    <BlockTitle title_text="Rólam"/>
    <IntroductionBlock/>
    <BlockTitle title_text="Ismereteim"/>
    <Stack/>
  </div>
</template>

<script>
import BasicInformation from './components/BasicInformation.vue'
import BlockTitle from './components/BlockTitle.vue'
import IntroductionBlock from './components/IntroductionBlock.vue'
import Navbar from './components/Navbar.vue'
import Stack from './components/Stack.vue'


export default {
  provide: {
    language: 'english'
  },
  name: 'App',
  components: {
    BasicInformation,
    BlockTitle,
    IntroductionBlock,
    Navbar,
    Stack
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
