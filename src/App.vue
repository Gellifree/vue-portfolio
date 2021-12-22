<template>
  <div class="container border bg-light">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Thi is a direct messahge from the App.vue file."/>
    <BasicInfomration/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import BasicInfomration from './components/BasicInfomration.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    BasicInfomration
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
