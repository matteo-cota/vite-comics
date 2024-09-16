<template>
  <div>
    <HeaderComponent />
    <MainContent /> 
    <BlueBarComponent />   
    <FooterComponent />
    
  </div>
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue';
import MainContent from './components/MainContent.vue';
import BlueBarComponent from './components/BlueBarComponent.vue';
import FooterComponent from './components/FooterComponent.vue';

export default {
  components: {
    HeaderComponent,
    MainContent,
    BlueBarComponent,   
    FooterComponent, 
  },
};
</script>

<style>

</style>