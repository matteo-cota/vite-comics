<template>
    <footer>
      <div class="footer-section">       
        <div class="footer-links">
          <h3>DC COMICS</h3>
          <ul>
            <li v-for="(item, index) in dcComicsLinks" :key="index">
              <a href="#">{{ item }}</a>
            </li>
          </ul>
        </div>
        <div class="footer-links">
          <h3>DC</h3>
          <ul>
            <li v-for="(item, index) in dcLinks" :key="index">
              <a href="#">{{ item }}</a>
            </li>
          </ul>
        </div>
        <div class="footer-links">
          <h3>SITES</h3>
          <ul>
            <li v-for="(item, index) in sitesLinks" :key="index">
              <a href="#">{{ item }}</a>
            </li>
          </ul>
        </div>
        <img class="logo" src="/img/dc-logo-bg.png" alt="">
      </div>      
      <div class="signup">
        <button>SIGN-UP NOW!</button>
        
        <div class="social-icons">
          <p>FOLLOW US</p>
          <img src="/img/footer-facebook.png" alt="">
          <img src="/img/footer-twitter.png" alt="">
          <img src="/img/footer-youtube.png" alt="">
          <img src="/img/footer-pinterest.png" alt="">
          <img src="/img/footer-periscope.png" alt="">
        </div>
      </div>
    </footer>
  </template>
  
  <script>
  export default {
    data() {
      return {
        dcComicsLinks: ['Characters', 'Comics', 'Movies', 'TV', 'Games', 'Videos', 'News'],
        dcLinks: ['Terms Of Use', 'Privacy Policy', 'Ad Choices', 'Advertising', 'Jobs', 'Subscriptions'],
        sitesLinks: ['DC', 'MAD Magazine', 'DC Kids', 'DC Universe', 'DC Power Visa'],
      };
    },
  };
  </script>
  
  <style scoped>
  footer {
    background-color: #3e3333;
    color: white;    
    margin: -8px;
  }
  .footer-section {
    display: flex;
    justify-content: space-around;  
    background-image: url(/img/footer-bg.jpg);  
    background-size: 50%;
  }
  .footer-links ul {
    list-style: none;
  }
  .footer-links a {
    color: white;
    text-decoration: none;
  }

  .footer-links{
    display: flex;
    flex-direction: column;
    align-items: center;

  }
  .signup {
    padding: 20px;
    display: flex;
    justify-content: space-around;
    align-items: center;
  }
  .signup button {
    background-color: transparent;
    color: white;
    padding: 10px 20px;
    border: solid;
    border-color: aqua;
    cursor: pointer;
  }
  
  .social-icons i {
    margin: 0 10px;
    font-size: 24px;
    color: white;
  }

  .social-icons{
    display: flex;
    align-items: center;
    gap:15px;
  }

  .logo {
    width: 25%;
  }

  p{
    color:#0076ff
  }
  </style>

