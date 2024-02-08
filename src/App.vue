<script>
import HeaderComp from './components/HeaderComp.vue';
import ComicsComp from './components/ComicsComp.vue';
import ServicesComp from './components/ServicesComp.vue';
import FooterIndex from './components/FooterIndex.vue';
import FooterSocials from './components/FooterSocials.vue';
import JumboComp from './components/JumboComp.vue';
export default{

  components:{
    HeaderComp,
    ComicsComp,
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
    <ComicsComp/>
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
