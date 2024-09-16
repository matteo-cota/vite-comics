<template>
  <div>
    <HeaderComponent />
    <MainContent />    
    
  </div>
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue';
import MainContent from './components/MainContent.vue';

export default {
  components: {
    HeaderComponent,
    MainContent,    
  },
};
</script>

<style>

</style>