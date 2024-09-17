<template>
    <div class="comics-grid">
      <div
        v-for="(comic, index) in comics"
        :key="index"
        class="comic-card"
      >
        <img :src="comic.thumb" :alt="comic.series" class="comic-card__image" />
        <div class="comic-card__content">
          <h3 class="comic-card__title">{{ comic.series }}</h3>
          <p class="comic-card__type">{{ comic.type }}</p>
          <p class="comic-card__price">{{ comic.price }}</p>
        </div>
      </div>
    </div>
  </template>
  
  <script>
 export default {
  name: 'ComicCard',
  data() {
    return {
      comics: []
    };
  },
  mounted() {
    fetch('/src/assets/dc-comics.json')
      .then(response => response.json())
      .then(data => {
        this.comics = data;
      })
      .catch(error => {
        console.error('Error fetching comics data:', error);
      });
  }
};
  </script>
  
  <style lang="scss">
  .comics-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(170px, 1fr));
    gap: 20px;
    padding: 20px;
    background-color: black;    
  }
  
  .comic-card {
    border: 1px solid #ddd;
    border-radius: 8px;
    overflow: hidden;
    max-width: 200px;
    transition: box-shadow 0.3s;
    
  
    &__image {
      width: 100%;
      height: auto;
    }
  
    &__content {
      padding: 16px;
      text-align: center;
  
      .comic-card__title {
        font-size: 1.2rem;
        margin-bottom: 8px;
      }
  
      .comic-card__type {
        color: #666;
        font-size: 0.9rem;
      }
  
      .comic-card__price {
        font-weight: bold;
        color: #333;
        margin-top: 8px;
      }
    }
  
    &:hover {
      box-shadow: 0px 4px 12px rgba(0, 0, 0, 0.1);
    }
  }
  </style>