<script>
import HeaderComp from './components/HeaderComp.vue';
import ContentComp from './components/ContentComp.vue';
import ServicesComp from './components/ServicesComp.vue';
import FooterIndex from './components/FooterIndex.vue';

export default{
  components:{
    HeaderComp,
    ContentComp,
    ServicesComp,
    FooterIndex,
  }
}

</script>


<template>

  <HeaderComp/>

  <main>
    <ContentComp/>
    <ServicesComp/>
  </main>

  <footer>
    <FooterIndex/>
  </footer>

</template>



<style lang="scss">
@use './assets/style/general'


</style>
