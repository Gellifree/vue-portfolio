<template lang="html">
  <div v-if="language['value'] == 'EN'">
    <CvTitle title="Tanulmányok" icon_type="fas fa-user-graduate"/>

    <CvBlock title="Programtervező Informatikus (Fejlesztő)" date="(2019 - ) Aktuális tanulmányok" :datas="hungarian_lang.cv_datas['eke_fosz']"/>
    <CvBlock title="Programtervező Informatikus Bsc" date="(2015 - 2019) Félbehagyott" :datas="hungarian_lang.cv_datas['eke_bsc']"/>
    <CvBlock title="Érettségi bizonyítvány" date="(2009 - 2014)" :datas="hungarian_lang.cv_datas['erettsegi']"/>



    <CvTitle title="Szakmai tapasztalat" icon_type="fas fa-briefcase"/>
      <CvBlock title="Dr.Code (Eger)" date="(2019 - 2021)" :datas="hungarian_lang.cv_datas['dr_code']"/>
      <CvBlock title="Alkalmi munkák/diákmunkák" date="(2014 - 2019)" :datas="hungarian_lang.cv_datas['alkalmi']"/>
    <CvTitle title="Személyes készségek" icon_type="fas fa-user-tie"/>
      <CvBlock title="Nyelvi készségek" date="" :datas="hungarian_lang.cv_datas['nyelv']"/>
      <CvBlock title="Kommunikációs készség" date="" :datas="hungarian_lang.cv_datas['komm']"/>
  </div>
  <div v-else>
    <CvTitle title="Studies" icon_type="fas fa-user-graduate"/>

    <CvBlock title="Software Information Technology" date="(2019 - ) Current studies" :datas="english_lang.cv_datas['eke_fosz']"/>
    <CvBlock title="Computer Science Ba/Bsc" date="(2015 - 2019) Abadoned" :datas="english_lang.cv_datas['eke_bsc']"/>
    <CvBlock title="General certificate of education " date="(2009 - 2014)" :datas="english_lang.cv_datas['erettsegi']"/>



    <CvTitle title="Professional experience" icon_type="fas fa-briefcase"/>
      <CvBlock title="Dr.Code (Eger)" date="(2019 - 2021)" :datas="english_lang.cv_datas['dr_code']"/>
      <CvBlock title="Casual work / student work" date="(2014 - 2019)" :datas="english_lang.cv_datas['alkalmi']"/>
    <CvTitle title="Personal skills" icon_type="fas fa-user-tie"/>
      <CvBlock title="Language skills" date="" :datas="english_lang.cv_datas['nyelv']"/>
      <CvBlock title="Communication skills" date="" :datas="english_lang.cv_datas['komm']"/>
  </div>

</template>

<script>
import CvBlock from './CvBlock.vue'
import CvTitle from './CvTitle.vue'

export default {
  components : {
    CvBlock,
    CvTitle
  },
  inject: ['language'],
  data() {
    return {
      hungarian_lang: {
        cv_datas: {
          'eke_fosz': ['Intézmény: Eszterházy Károly Katolikus Egyetem (Eger) ', 'Várható befejezés: 2022.06.30. ', 'Szint: felsőoktatási szakképzés ', 'Tagozat: Levelező '],
          'eke_bsc' : ['Intézmény: Eszterházy Károly Katolikus Egyetem (Eger) ', 'Félbehagyott tanulmányok ', 'Szint: Alapképzés (Ba/Bsc) ', 'Tagozat: Nappali '],
          'erettsegi' : ['Intézmény: Vak Bottyán János Katolikus Műszaki és Közgazdasági Középiskola és Kollégium (Gyöngyös) ', 'Tagozat: Nyelvi Informatika (Angol) '],
          'dr_code' : ['Dr.Code (Eger) ', 'Önkéntes oktató ', 'Tanított nyelvek: Scratch, C#, Python, GdScript (Godot) '],
          'alkalmi' : ['Deichmann Cipőkereskedelmi Kft.', 'Értékesítő', '', 'Robert Bosch Elektronika Kft.', 'Operátor, Karbantartó gyakornok'],
          'nyelv' :  ['Anyanyelv: Magyar ', 'Idegen nyelv: Angol ', 'Nyelvvizsgával nem rendelkezem, képességeim B2. szinttel jellemezhetőek. '],
          'komm' : ['A PR és Marketing munkacsoport vezetőjeként jó szervező, problémamegoldó és kommunikációs képességgel rendelkezem. ']
        }
      },
      english_lang: {
        cv_datas: {
          'eke_fosz': ['Institution: Eszterházy Károly Catholic University (Eger) ', 'Expected completion: June 30, 2022.', 'Level: higher education vocational training', 'Category: Correspondent'],
          'eke_bsc' : ['Institution: Eszterházy Károly Catholic University (Eger) ', 'Abandoned studies', 'Level: Undergraduate (Ba / Bsc)', 'Level: Regular'],
          'erettsegi' : ['Institution: Vak Bottyán János Catholic Technical and Economic Secondary School and College (Gyöngyös)', 'Type: Language Informatics (English)'],
          'dr_code' : ['Dr.Code (Eger) ', 'Volunteer instructor ', 'Languages ​​taught: Scratch, C#, Python, GdScript (Godot)'],
          'alkalmi' : ['Deichmann Shoe Trading Ltd.', 'Salesman', '', 'Robert Bosch GmbH', 'Operator, Maintenance Trainee'],
          'nyelv' :  ['Mother-tongue: Hungarian', 'Foreign language: English', 'I dont have a language exam, I would characterize my skills with B2 level.'],
          'komm' : ['As the leader of the PR and Marketing team, I have good organizing, problem solving and communication skills.']
        }
      }
    }
  }
}
</script>

<style lang="css" scoped>
</style>
