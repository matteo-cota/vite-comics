<template>
  <header>
    <div class="logo">
      <img src="/img/dc-logo.png" alt="DC Logo" />
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
header {
  display: flex;
  justify-content: space-between;
  padding: 20px;
  background-color: white;
}
.logo img {
  height: 60px;
}
nav ul {
  display: flex;
  list-style: none;
  gap: 20px;
}
nav ul li a {
  text-decoration: none;
  color: black;
  font-weight: bold;
}
</style>