<template>
  <div>
    <HeaderComponent />
    <MainContent /> 
    <BlueBarComponent />   
    
  </div>
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue';
import MainContent from './components/MainContent.vue';
import BlueBarComponent from './components/BlueBarComponent.vue';

export default {
  components: {
    HeaderComponent,
    MainContent,
    BlueBarComponent,    
  },
};
</script>

<style>

</style>