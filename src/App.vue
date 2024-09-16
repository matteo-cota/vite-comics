<template>
  <div>
    <HeaderComponent />
    <BlueBarComponent />
    <MainContent />
    <FooterComponent />
  </div>
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue';
import BlueBarComponent from './components/BlueBarComponent.vue';
import MainContent from './components/MainContent.vue';
import FooterComponent from './components/FooterComponent.vue';

export default {
  components: {
    HeaderComponent,
    BlueBarComponent,
    MainContent,
    FooterComponent,
  },
};
</script>

<style>

</style>