<template lang="html">
  <div class="bg-white shadow-sm border p-3 rounded my-3 mx-auto row container">
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
          'description' : 'A Linux rendszerek használata hozta magával, elsősorban konzolos alkalmazások készítésére használom, de van minimális tapasztalatom Gtk alkalmazások készítésében is.'
        },
        {
          'title' : 'HTML 5, CSS, Javascript, Bootstrap',
          'description' : 'A webfejlesztés alapjai véleményem szerint elengedhetetlenek. A Javascript funcionális megközelítése még távol áll tőlem, de procedurálisan jó alapjaim vannak.'
        },
        {
          'title' : 'C / C++',
          'description' : 'Kevés gyakorlattal rendelkezek, de a jövőben szeretnék több C/C++ projektet készíteni.'
        },
        {
          'title' : 'Shell script',
          'description' : 'A Linuxok hétköznapi használata magával hozott egy felületes Shell script ismeretet, otthonosan mozgok a terminálban.'
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
          'description' : 'Az egyetemen először tanult programozási nyelvem. A Linuxok mellett erősen háttérbe szorult, és nem igazán volt rá szükségem, de erős OOP alapokat adott.'
        },
        {
          'title' : 'GdScript / Godot',
          'description' : 'Ha játékfejlesztésről van szó, számomra Linuxon a Godot nyújtja a megfelelő eszközöket. Sajnos kevesebb időm van foglalkozni vele, mint amennyit szeretnék. A GdScript szinte teljes mértékben megeggyezik a Pythonnal.'
        },
        {
          'title' : 'Alternatív programok',
          'description' : 'Az Adobe programjai helyett, többnyire ingyenes, nyílt forráskódú szoftvereket használok a munkáim során. (Inkscape, Krita, Kdenlive, Enve stb.)'
        },
        {
          'title' : 'MySQL',
          'description' : 'Véleményem szerint az SQL egy olyan alapvető tudás, amit minden programozónak ismernie kell. Természetesen még rengeteget kell fejlődnöm, jelenleg csak MySQL-el van tapasztalatom.'
        },
        {
          'title' : 'Git / Github',
          'description' : 'Kissé feleslegesnek érzem feltüntetni, a verziókezelő használata is olyan alapvető képesség amire hétköznapi szinten szükség van.'
        },
        {
          'title' : 'Vue.js',
          'description' : 'Az első keretrendszer amit elkezdtem tanulni, és nagyon szimpatikus számomra a működése.'
        }
      ]
    }
  }
}
</script>

<style lang="css" scoped>
</style>
