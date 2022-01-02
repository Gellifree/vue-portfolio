<template lang="html">
  <div class="bg-white shadow-sm border p-3 rounded my-3 mx-0 row">
    <div class="col mt-3" v-for="(value, key) in skills" :key="key">
      <StackBlock class="mx-auto" :stack_title="value.title" :stack_description="value.description"/>
    </div>
  </div>
</template>

<script>
import StackBlock from './StackBlock.vue'
export default {
  components: {
    StackBlock
  },
  data() {
    return {
      skills: [
        {
          'title' : 'Python 3',
          'description' : 'Elsősorban a Linux rendszerek használata hozta magával, elsősorban konzolos alkalmazások készítésére használom, de van minimális tapasztalatom Gtk alkalmazások készítésében is.'
        },
        {
          'title' : 'HTML 5, CSS, Javascript',
          'description' : 'Alapszintű tapasztalattal rendelkezem, Bootstrap-et és Vue.js-t használok.'
        },
        {
          'title' : 'C/C++',
          'description' : 'Kevés gyakorlattal rendelkezek, de a jövőben szeretnék több C/C++ projektet készíteni.'
        },
        {
          'title' : 'Shell script',
          'description' : 'A Linuxok hétköznapi használata magával hozott egy felületes Shell script ismeretet.'
        },
        {
          'title' : 'Codeigniter keretrendszer',
          'description' : 'Ebben a keretrendszerben készítem a szakdolgozatomat, bár belátásom szerint kevés helyen használják, ezért bizonytalan vagyok abban, hogy a továbbiakban mélyítsem-e a tudásomat benne, vagy használjak olyan keretrendszert, aminek nagyobb a jelenléte.'
        },
        {
          'title' : 'LaTeX',
          'description' : 'A hétköznapi életemhez tartozik a dokumentációkészítés, és a LaTeX-nél jobb eszközt elképzelni sem tudnék erre a feladatra. '
        },
        {
          'title' : 'C Sharp (C#)',
          'description' : 'Az egyetemen először tanult programozási nyelvem. A Linuxok mellett erősen háttérbe szorult, és nem igazán volt rá szükségem.'
        },
        {
          'title' : 'GdScript/Godot',
          'description' : 'Ha játékfejlesztésről van szó, számomra Linuxon a Godot nyújtja a megfelelő eszközöket. Sajnos kevesebb időm van foglalkozni vele, mint amennyit szeretnék. A GdScript szinte teljes mértékben megeggyezik a Pythonnal.'
        },
        {
          'title' : 'Alternatív programok',
          'description' : 'Az Adobe programjai helyett, többnyire ingyenes, nyílt forráskódú szoftvereket használok a munkáim során. (Inkscape, Krita, Kdenlive, Enve stb.)'
        }
      ]
    }
  }
}
</script>

<style lang="css" scoped>
</style>
