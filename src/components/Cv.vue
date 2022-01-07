<template lang="html">
  <CvTitle title="Tanulmányok" icon_type="fas fa-user-graduate"/>

  <CvBlock title="Programtervező Informatikus (Fejlesztő)" date="(2019 - ) Aktuális tanulmányok" :datas="cv_datas['eke_fosz']"/>
  <CvBlock title="Programtervező Informatikus Bsc" date="(2015 - 2019) Félbehagyott" :datas="cv_datas['eke_bsc']"/>
  <CvBlock title="Érettségi bizonyítvány" date="(2009 - 2014)" :datas="cv_datas['erettsegi']"/>



  <CvTitle title="Szakmai tapasztalat" icon_type="fas fa-briefcase"/>
    <CvBlock title="Dr.Code (Eger)" date="(2019 - 2021)" :datas="cv_datas['dr_code']"/>
    <CvBlock title="Alkalmi munkák/diákmunkák" date="(2014 - 2019)" :datas="cv_datas['alkalmi']"/>
  <CvTitle title="Személyes készségek" icon_type="fas fa-user-tie"/>
    <CvBlock title="Nyelvi készségek" date="" :datas="cv_datas['nyelv']"/>
    <CvBlock title="Kommunikációs készség" date="" :datas="cv_datas['komm']"/>
</template>

<script>
import CvBlock from './CvBlock.vue'
import CvTitle from './CvTitle.vue'

export default {
  components : {
    CvBlock,
    CvTitle
  },
  data() {
    return {
      cv_datas: {
        'eke_fosz': ['Intézmény: Eszterházy Károly Katolikus Egyetem (Eger) ', 'Várható befejezés: 2022.06.30. ', 'Szint: felsőoktatási szakképzés ', 'Tagozat: Levelező '],
        'eke_bsc' : ['Intézmény: Eszterházy Károly Katolikus Egyetem (Eger) ', 'Félbehagyott tanulmányok ', 'Szint: Alapképzés (Ba/Bsc) ', 'Tagozat: Nappali '],
        'erettsegi' : ['Intézmény: Vak Bottyán János Katolikus Műszaki és Közgazdasági Középiskola és Kollégium (Gyöngyös) ', 'Tagozat: Nyelvi Informatika (Angol) '],
        'dr_code' : ['Dr.Code (Eger) ', 'Önkéntes oktató ', 'Tanított nyelvek: Scratch, C#, Python, GdScript (Godot) '],
        'alkalmi' : ['Deichmann Cipőkereskedelmi Kft.', 'Értékesítő', '', 'Robert Bosch Elektronika Kft.', 'Operátor, Karbantartó gyakornok'],
        'nyelv' :  ['Anyanyelv: Magyar ', 'Idegen nyelv: Angol ', 'Nyelvizsgával nem rendelkezem, képességeim B2. szinttel jellemezhetőek. '],
        'komm' : ['A PR és Marketing munkacsoport vezetőjeként jó szervező, problémamegoldó és kommunikációs képességgel rendelkezem. ']
      }
    }
  }
}
</script>

<style lang="css" scoped>
</style>
