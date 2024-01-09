<script>
import Appheader from './components/Appheader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';
export default {
  components : {
    AppFooter,
    AppMain,
    Appheader
  }
      
}
</script>
<template lang="">
  <div>
    <Appheader />
    <AppMain />
    <AppFooter />
  </div>
</template>
<style lang="scss">
  @use './styles/partials/variables';
  @use './styles/generals.scss' ;
  
</style>