<template lang="html">
  <div class="bg-white shadow-sm border p-3 rounded my-3 mx-auto row container" v-if="language['value'] == 'EN'">
    <div class="col mt-3" v-for="(value, key) in hungarian_lang.skills" :key="key">
      <StackBlock class="mx-auto" :stack_title="value.title" :stack_description="value.description"/>
    </div>
  </div>
  <div class="bg-white shadow-sm border p-3 rounded my-3 mx-auto row container" v-else>
    <div class="col mt-3" v-for="(value, key) in english_lang.skills" :key="key">
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
  inject: ['language'],
  data() {
    return {
      hungarian_lang: {
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
      },
      english_lang: {
        skills: [
          {
            'title' : 'Python 3',
            'description' : 'It comes with the use of Linux systems, I mainly use it to build console applications, but I also have minimal experience in building Gtk applications.'
          },
          {
            'title' : 'HTML 5, CSS, Javascript, Bootstrap',
            'description' : 'The basics of web development are essential in my opinion. The functional approach to Javascript is still far from me, but I have a good procedural foundation.'
          },
          {
            'title' : 'C / C++',
            'description' : 'I have little experience, but I want to create more C / C ++ projects in the future.'
          },
          {
            'title' : 'Shell script',
            'description' : 'Everyday use of Linux has brought with it a superficial knowledge of Shell scripting.'
          },
          {
            'title' : 'Codeigniter framework',
            'description' : 'I write my dissertation in this framework, although it seems to be used in a few places, so I am unsure whether to further deepen my knowledge in it or use a framework with a greater presence.'
          },
          {
            'title' : 'LaTeX',
            'description' : 'Documentation is part of my everyday life, and I couldn’t imagine a better tool for this task than LaTeX.'
          },
          {
            'title' : 'C Sharp (C#)',
            'description' : 'This language was my first programming language at university. In addition to Linux, it was heavily relegated to the background and I didn’t really need it, but it provided a strong foundation for OOP.'
          },
          {
            'title' : 'GdScript / Godot',
            'description' : 'When it comes to game development, for me, Godot provides the right tools on Linux. Unfortunately, I can spend less time on it than I would like. GdScript is almost identical to Python.'
          },
          {
            'title' : 'Alternative programs',
            'description' : 'Instead of Adobe programs, I mostly use free, open source software in my work. (Inkscape, Krita, Kdenlive, Enve, etc.)'
          },
          {
            'title' : 'MySQL',
            'description' : 'In my opinion, SQL is a basic knowledge that every programmer should know. Of course, I still have a lot to develop, I currently only have experience with MySQL.'
          },
          {
            'title' : 'Git / Github',
            'description' : 'I find it a bit unnecessary to point out, using the version control is also a basic skill that is needed on a day-to-day basis.'
          },
          {
            'title' : 'Vue.js',
            'description' : 'The first frontend framework I started learning and I want to deepen my knowledge in it.'
          }
        ]
      },
    }
  }
}
</script>

<style lang="css" scoped>
</style>
