<template>
    <div class="blue-bar">
      <div v-for="(icon, index) in icons" :key="index" class="icon-item">
        <img :src="icon.img" :alt="icon.title" />
        <p>{{ icon.title }}</p>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        icons: [
          { title: 'Digital Comics', img: '/img/buy-comics-digital-comics.png' },
          { title: 'DC Merchandise', img: 'img/buy-comics-merchandise.png' },
          { title: 'Subscription', img: '/img/buy-comics-subscriptions.png' },
          { title: 'Comic Shop Locator', img: '/img/buy-comics-shop-locator.png' },
          { title: 'DC Power Visa', img: '/img/buy-dc-power-visa.svg' },
        ],
      };
    },
  };
  </script>
  
  <style scoped>
  .blue-bar {
    display: flex;
    justify-content: space-around;
    background-color: #0076ff;
    padding: 20px 0;
    align-items: baseline;
    margin: -8px;
}
  
  .icon-item {
    text-align: center;
    color: white;
  }
  .icon-item img {
    max-width: 30px;
  }
  </style>