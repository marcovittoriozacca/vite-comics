<script>
import HeaderComp from './components/HeaderComp.vue';
import ContentComp from './components/ContentComp.vue';
import ServicesComp from './components/ServicesComp.vue';

export default{
  components:{
    HeaderComp,
    ContentComp,
    ServicesComp,
  }
}

</script>


<template>

  <HeaderComp/>

  <main>
    <ContentComp/>
    <ServicesComp/>
  </main>

</template>



<style lang="scss">
@use './assets/style/general'


</style>
