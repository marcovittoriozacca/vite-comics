<script>
import HeaderComp from './components/HeaderComp.vue';
import ContentComp from './components/ContentComp.vue';

export default{
  components:{
    HeaderComp,
    ContentComp,
  }
}

</script>


<template>

  <HeaderComp/>

  <main>
    <ContentComp/>
  </main>

</template>



<style lang="scss">
@use './assets/style/general'


</style>
