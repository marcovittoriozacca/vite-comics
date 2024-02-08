<script>
import HeaderComp from './components/HeaderComp.vue';
import ContentComp from './components/ContentComp.vue';
import ServicesComp from './components/ServicesComp.vue';
import FooterIndex from './components/FooterIndex.vue';
import FooterSocials from './components/FooterSocials.vue';
import JumboComp from './components/JumboComp.vue';
export default{

  components:{
    HeaderComp,
    ContentComp,
    ServicesComp,
    FooterIndex,
    FooterSocials,
    JumboComp,
  }
  
}

</script>


<template>

  <HeaderComp/>

  <main>
    <JumboComp/>
    <ContentComp/>
    <ServicesComp/>
  </main>

  <footer>
    <FooterIndex/>
    <FooterSocials/>
  </footer>

</template>



<style lang="scss">
@use './assets/style/general'


</style>
