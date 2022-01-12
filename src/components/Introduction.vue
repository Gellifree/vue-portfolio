<template lang="html">
  <div class="bg-white shadow-sm border p-3 rounded my-3" v-if="language['value'] == 'EN'">
    <h5 class="text-secondary">Bemutatkozás</h5>
    <p class="text-secondary medium-text"> {{ hungarian_lang.first_text_block }}</p>
    <p class="text-secondary medium-text"> {{ hungarian_lang.second_text_block }}</p>
    <p class="text-secondary medium-text" v-for="text in hungarian_lang.introduction_texts" :key="text.id">
      <span v-if="block_open">{{ text }}</span>
    </p>
    <button type="button" name="button" class="btn btn-info text-white" @click="block_open = !block_open">
      <span v-if="block_open">Bezár</span>
      <span v-else>Lenyit</span>
    </button>
  </div>
  <div class="bg-white shadow-sm border p-3 rounded my-3" v-else>
    <h5 class="text-secondary">Introduction</h5>
    <p class="text-secondary medium-text"> {{ english_lang.first_text_block }}</p>
    <p class="text-secondary medium-text"> {{ english_lang.second_text_block }}</p>
    <p class="text-secondary medium-text" v-for="text in english_lang.introduction_texts" :key="text.id">
      <span v-if="block_open">{{ text }}</span>
    </p>
    <button type="button" name="button" class="btn btn-info text-white" @click="block_open = !block_open">
      <span v-if="block_open">Close</span>
      <span v-else>Open</span>
    </button>
  </div>
</template>

<script>
export default {
  name: 'Basic Inftroduction Component',
  inject: ['language'],
  data() {
    return {
      hungarian_lang: {
        first_text_block: 'Kovács Norbert vagyok, egyetemista az Eszterházy Károly Katolikus egyetemen. Programtervező informatika szakon tanulok. A Roma Szakkollégium tagja vagyok, a PR és Marketing munkacsoport vezetője. A legfontosabb számomra, hogy az egyetem befejezése előtt olyan munkahelyet találjak, ahol szakmailag kiteljesedhetek és tovább fejleszthetem magam.',
        second_text_block: 'Az egyetemen tanult első programozási nyelv a C# volt. Évekig nem is tanultam más programozási nyelvet, próbáltam elmélyíteni az objektumorientált gondolkodásmód részleteit. Fiatalkorom óta szimpatizáltam a Linux rendszerekkel, és ez az egyetemen csak felerősödött. Ez magával hozta a Python nyelv szeretetét, mivel rendkívül kényelmes és gyors Pythonnal fejleszteni. Teljesen elhagytam a Windows rendszerek használatát, ami ugyan sok kompromisszummal jár, de összességében, nem tudnám elképzelni, hogy ne valamilyen Ubuntu, vagy Arch alapú rendszert használjak a hétköznapokban. Idővel elkezdtem statikus weboldalakat készíteni, majd megismerkedtem a PHP alapjaival. A Codeigniter keretrendszer számomra sokkal értékesebbé tette a php nyelvet. A különböző weboldalak készítése magával hozta a bootstrap használatát. Ezektől elrugaszkodva szabadidőmben megismerkedtem a Godot játékmotorral. A Godot könnyen kezelhető, logikusan felépített és kifejezetten egyszerűen elkészíthetőek alkalmazások, játékok benne. ',
        introduction_texts: [
          'A Microsoft irodai programcsomagjának elhagyása, és az alternatív programok használata, néha igen csak sok nehézséget tud okozni. Természetesen, rengeteg alternatív lehetőség nyújtott, azonban egyik sem tökéletes. Természetesen ez az online eszközökkel kikerülhető, de ez sem mindig megoldás. Összességében, amikor lehetőségem van rá, minden szövegszerkesztőt kerülök, és a dokumentumokat TeXStudio-ban készítem el, gyorsan, egységes minőségű PDF dokumentumként. Az Adobe programcsomagjai helyett, ingyenes, nyílt forráskódú alternatíváikat használom.',
          'A második nekifutásom az egyetemi életnek, szorosan összekötődik az Roma Szakkollégiummal. Nehéz élethelyzetemből adódóan, lehetőségem lett jelentkezni. Bekerülésem óta, a Pr és Marketing munkacsoport tagja, immáron vezetője vagyok két éve. Rengeteg tapasztalatot adott számomra a szervezet, betekintést nyerhettem a belső működésbe. Munkacsoport vezetőként sokszor besegítek a videóvágásban, és a forgatásokat is én vezényelem. A munkacsoport vezetése, a dokumentáció készítésének, és a féléves szakmai terveken túl, megtanított arra, hogyan gazdálkodjak a munkacsoport tagjainak erőforrásaival, legyen az idő, vagy információ. Így született meg az órarend elemző prototípus program, és a szakdolgozatom is egy nyilvántartó webalkalmazás, a szervezet számára. ',
          'Egy szintén nagyon fontos része az életem ezen részének, a Dr.Code-nál végzett önkéntes munka. Két és fél évig tanítottam önkéntesként a Dr.Code-nál. A munkalehetőség igen sok kihívást rejtett, de sikerült felülkerekednem ezeken. Először Scratch-et tanítottam, általános iskolásoknak, majd később C#-ot Unityhez. Ezenkívül sikerült egy Python, majd Godot kurzust is indítani amiben részt vettem. Hosszútávon kiderült hogy az idősebb (7. osztálytól felfelé) korosztállyal jobban megy a tanítás. Velük sikerült megtalálni a közös hangot és a motivációt. ',
          ' Minimális c/c++ ismeretekkel rendelkezek, de nincs egyetlen nagyobb projektem sem, amire támaszkodhatnék. A Java nyelv, alapvetően közel áll hozzám, a több éves C# tapasztalat miatt, viszont erre a nyelvre sem volt még különösebben szükségem. ',
          'A napjaimat azzal töltöm, hogy próbálom fejleszteni önmagam, és a jelenlegi tudásomat próbálom mélyíteni. Szabadidőmben a Codeigniter keretrendszerrel szeretnék, valódi problémákat megoldó webalkalmazásokat készíteni, a Godot motor segítségével pedig játékokat készíteni. Tisztában vagyok vele, hogy rengeteg tudást, és technológiát kell még elsajátítanom, és a jelenlegi ismerteimet pedig profi szintre kell emelni. '
        ]
      },
      english_lang: {
        first_text_block: 'I am Norbert Kovács, a student at the Eszterházy Károly Catholic University. I am studying program design informatics. I am a member of the Roma College and head of the PR and Marketing working group. The most important thing before I graduate from university is to find a job where I can complete professionally and further develop myself.',
        second_text_block: 'The first programming language I studied at university was C#. I didn’t even learn another programming language for years, I tried to deepen the details of the object-oriented way of thinking. I’ve been sympathetic to Linux since I was a kid, and it just got stronger at university. This brought with it a love of the Python language as it is extremely convenient and fast to develop with Python. I have completely abandoned the use of Windows systems, which involves a lot of compromises, but overall, I could not imagine not using some Ubuntu or Arch based system in everyday life. Over time, I started building static web pages and then learned the basics of PHP. The Codeigniter framework made php much more valuable to me. Creating different websites brought with it the use of bootstrap. Breaking away from these, I became acquainted with the Godot game engine in my spare time. Godot is easy to use, logically structured and very easy to create applications and games.',
        introduction_texts: [
          'Leaving Microsoft office suite and using alternative programs can sometimes cause a lot of difficulty. Of course, there were plenty of alternatives, but none were perfect. Of course, this can be avoided with online tools, but this is not always a solution either. Overall, when I have the opportunity, I avoid all word processors and create documents in TeXStudio, quickly, as a consistent quality PDF document. Instead of Adobe software packages, I use their free, open source alternatives.',
          'My second run into university life is closely linked to the Roma College. Due to my difficult life situation, I had the opportunity to apply. Since joining, I have been a member of the PR and Marketing team and have been the leader for two years now. The organization gave me a lot of experience, I was able to gain insight into the internal operation. As a team leader, I often help with video editing, and I also direct the filming. In addition to preparing the documentation and the semi-annual professional plans, the leadership of the team taught me how to manage the resources of the team members, be it time or information. This is how the timetable analysis prototype program was born, and my dissertation is also a registry web application for the organization.',
          'Another very important part of this part of my life is volunteering at Dr.Code. I taught as a volunteer at Dr.Code for two and a half years. The job opportunity had a lot of challenges, but I managed to overcome them. I first taught Scratch to elementary school students and later C # to Unity. I also managed to launch a Python and then Godot course which I attended. In the long run, it has been found that teaching goes better with the older age group (from 7th grade onwards). They managed to find common ground and motivation with them.',
          'I have minimal c / c ++ knowledge, but I don t have any major projects to rely on. The Java language is basically close to me because of my many years of C # experience, but I didn’t particularly need that language.',
          'I spend my days trying to improve myself and deepen my current knowledge. In my spare time, I want to use the Codeigniter framework to build web applications that solve real problems, and the Godot engine to build games. I am aware that I still have a lot of knowledge and technology to master and that my current knowledge needs to be raised to a professional level.'
        ]
      },
      block_open: false
    }
  }
}
</script>

<style lang="css" scoped>
</style>
