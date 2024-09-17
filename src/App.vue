<template>
  <div>
    <HeaderComponent />    
    <MainContent /> 
    <ComicCard />
    <BlueBarComponent />   
    <FooterComponent />
    
    
  </div>
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue';
import MainContent from './components/MainContent.vue';
import ComicCard from './components/ComicCard.vue';
import BlueBarComponent from './components/BlueBarComponent.vue';
import FooterComponent from './components/FooterComponent.vue';


export default {
  components: {
    HeaderComponent,    
    MainContent,
    ComicCard,
    BlueBarComponent,   
    FooterComponent, 
    
  },
};
</script>

<style>

</style>