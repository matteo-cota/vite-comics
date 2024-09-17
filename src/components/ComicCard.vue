<template>
    <div class="comics-grid">
        <button class="current">CURRENT SERIES</button>
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
      <button class="load">LOAD MORE</button>
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
    grid-template-columns: repeat(auto-fill, minmax(180px, 2fr));
    gap: 20px;
    padding: 20px;
    background-color: #252525    
  }

  .load {
    POSITION: relative;
    top: 0;
    left: 274%;
    width: 200px;
    height: 2pc;
    background-color: #0076ff;
    border: none;
  }

  .current {
    padding: 13px;
    width: 13%;
    height: 5%;
    display: flex;
    position: absolute;
    justify-content: space-around;
    top: 368px;
    align-items: center;
    background-color: #0076ff;
    color: white;
    border: none;
  }
  .current button {
    background-color: transparent;
    color: white;
    padding: 10px 20px;
    border: solid;
    border-color: aqua;
    cursor: pointer;
  }
  
  .comic-card {    
    border-radius: 8px;
    overflow: hidden;
    max-width: 180px;
    transition: box-shadow 0.3s;
    
  
    &__image {
      width: 100%;
      height: 50%;
    }
  
    &__content {
      padding: 16px;
      text-align: center;
  
      .comic-card__title {
        font-size: 0.9rem;
        margin-bottom: 8px;
        color: white;
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