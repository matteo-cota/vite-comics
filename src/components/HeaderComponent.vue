<template>
    <header>
      <div class="logo">
        <img src="/img/dc-logo.png" alt="Logo DC" />
      </div>
      <nav>
        <ul>
          <li v-for="(item, index) in menuItems" :key="index">
            <a href="#">{{ item }}</a>
          </li>
        </ul>
      </nav>
    </header>
  </template>
  
  <script>
  export default {
    data() {
      return {
        menuItems: ['Characters', 'Comics', 'Movies', 'TV', 'Games', 'Collectibles', 'Videos', 'Fans', 'News', 'Shop'],
      };
    },
  };
  </script>
  
  <style scoped>
  
  </style>