<template lang="html">
  <div class="bg-white shadow-sm border p-3 rounded my-3">
    <p class="text-secondary medium-text"> {{ first_text_block }}</p>
    <p class="text-secondary medium-text" v-for="text in introduction_texts" :key="text.id">
      <span v-if="block_open">{{ text }}</span>
    </p>
    <button type="button" name="button" class="btn btn-info text-white" @click="Toggleblock">
      <span v-if="block_open">Bezár</span>
      <span v-else>Lenyit</span>
    </button>
  </div>
</template>

<script>
export default {
  methods: {
    Toggleblock() {
      this.block_open = !this.block_open
    }
  },
  data() {
    return {
      first_text_block:         'Kovács Norbert vagyok, egyetemista az Eszterházy Károly Katolikus egyetemen. Programtervező informatika szakon tanulok. A Roma Szakkollégium tagja vagyok, a PR és Marketing munkacsoport vezetője. A legfontosabb számomra, hogy az egyetem befejezése előtt olyan munkahelyet találjak, ahol szakmailag kiteljesedhetek és tovább fejleszthetem magam.',
      introduction_texts: [
        'Az egyetemen tanult első programozási nyelv a C# volt. Évekig nem is tanultam más programozási nyelvet, próbáltam elmélyíteni az objektumorientált gondolkodásmód részleteit. Fiatalkorom óta szimpatizáltam a Linux rendszerekkel, és ez az egyetemen csak felerősödött. Ez magával hozta a Python nyelv szeretetét, mivel rendkívül kényelmes és gyors Pythonnal fejleszteni. Teljesen elhagytam a Windows rendszerek használatát, ami ugyan sok kompromisszummal jár, de összességében, nem tudnám elképzelni, hogy ne valamilyen Ubuntu, vagy Arch alapú rendszert használjak a hétköznapokban. Idővel elkezdtem statikus weboldalakat készíteni, majd megismerkedtem a PHP alapjaival. A Codeigniter keretrendszer számomra sokkal értékesebbé tette a php nyelvet. A különböző weboldalak készítése magával hozta a bootstrap használatát. Ezektől elrugaszkodva szabadidőmben megismerkedtem a Godot játékmotorral. A Godot könnyen kezelhető, logikusan felépített és kifejezetten egyszerűen elkészíthetőek alkalmazások, játékok benne. ',
        'A Microsoft irodai programcsomagjának elhagyása, és az alternatív programok használata, néha igen csak sok nehézséget tud okozni. Természetesen, rengeteg alternatív lehetőség nyújtott, azonban egyik sem tökéletes. Természetesen ez az online eszközökkel kikerülhető, de ez sem mindig megoldás. Összességében, amikor lehetőségem van rá, minden szövegszerkesztőt kerülök, és a dokumentumokat TeXStudio-ban készítem el, gyorsan, egységes minőségű PDF dokumentumként. Az Adobe programcsomagjai helyett, ingyenes, nyílt forráskódú alternatíváikat használom.',
        'A második nekifutásom az egyetemi életnek, szorosan összekötődik az Roma Szakkollégiummal. Nehéz élethelyzetemből adódóan, lehetőségem lett jelentkezni. Bekerülésem óta, a Pr és Marketing munkacsoport tagja, immáron vezetője vagyok két éve. Rengeteg tapasztalatot adott számomra a szervezet, betekintést nyerhettem a belső működésbe. Munkacsoport vezetőként sokszor besegítek a videóvágásban, és a forgatásokat is én vezényelem. A munkacsoport vezetése, a dokumentáció készítésének, és a féléves szakmai terveken túl, megtanított arra, hogyan gazdálkodjak a munkacsoport tagjainak erőforrásaival, legyen az idő, vagy információ. Így született meg az órarend elemző prototípus program, és a szakdolgozatom is egy nyilvántartó webalkalmazás, a szervezet számára. ',
        'Egy szintén nagyon fontos része az életem ezen részének, a Dr.Code-nál végzett önkéntes munka. Két és fél évig tanítottam önkéntesként a Dr.Code-nál. A munkalehetőség igen sok kihívást rejtett, de sikerült felülkerekednem ezeken. Először Scratch-et tanítottam, általános iskolásoknak, majd később C#-ot Unityhez. Ezenkívül sikerült egy Python, majd Godot kurzust is indítani amiben részt vettem. Hosszútávon kiderült hogy az idősebb (7. osztálytól felfelé) korosztállyal jobban megy a tanítás. Velük sikerült megtalálni a közös hangot és a motivációt. ',
        ' Minimális c/c++ ismeretekkel rendelkezek, de nincs egyetlen nagyobb projektem sem, amire támaszkodhatnék. A Java nyelv, alapvetően közel áll hozzám, a több éves C# tapasztalat miatt, viszont erre a nyelvre sem volt még különösebben szükségem. ',
        'A napjaimat azzal töltöm, hogy próbálom fejleszteni önmagam, és a jelenlegi tudásomat próbálom mélyíteni. Szabadidőmben a Codeigniter keretrendszerrel szeretnék, valódi problémákat megoldó webalkalmazásokat készíteni, a Godot motor segítségével pedig játékokat készíteni. Tisztában vagyok vele, hogy rengeteg tudást, és technológiát kell még elsajátítanom, és a jelenlegi ismerteimet pedig profi szintre kell emelni. '
      ],
      block_open: false
    }
  }
}
</script>

<style lang="css" scoped>
</style>
