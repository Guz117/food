<template>
  <div class="footer">
    <div class="center-footer">
      <div class="img-footer">
        <img :src="require('../assets/images/avada-food-logo-mob.png')" alt="">
        <ul class="ul-social">
              <li class="social"><a href="#"><i class="fab fa-facebook-f"></i></a></li>
              <li class="social"><a href="#"><i class="fab fa-instagram"></i></a></li>
              <li class="social"><a href="#"><i class="fab fa-twitter"></i></a></li>
              <li class="social"><a href="#"><i class="fab fa-youtube"></i></a></li>
          </ul>
      </div>
      <div class="nav-footer">
        <ul class="ul-footer">
          <li v-for="(linkNav, index) in linksNav"
          :key="index"
          ><a
          :href="linkNav.url">{{ linkNav.text }}</a></li>
      </ul>
      </div>
      <div class="contact">
        <p id="contact-title">CONTACT</p>
        <ul>
          <li><i class="fas fa-map-marker-alt"></i><p>775 New York Ave, Brooklin, Kings, New York 11203</p></li>
          <li><i class="fas fa-phone"></i><p>+0100-505-0000</p></li>
          <li><i class="fas fa-envelope"></i><p>info@your-domain.com</p></li>
        </ul>
      </div>
      <div class="app">
        <p id="app-title">GET OUR APP</p>
        <img :src="require('../assets/images/download-android.png')" alt="">
        <img :src="require('../assets/images/download-app-store.png')" alt="">
      </div>
    </div>
    <div class="copyright">
      <a href="#start"><i class="fas fa-chevron-up"></i></a>
      <p>&#169; Copyright 2012-2020 | Avada Theme by ThemeFusion | All Rights Reserved | Powered by WordPress</p>
    </div>

  </div>
</template>

<script>
export default {
    name: 'Footer',
    data() { 
    return {
      linksNav: [
                {
                    text: "Home",
                    url: "#",
                    current: true,
                },
                {
                    text: "Recepies",
                    url: "#",
                    current: false,
                },
                {
                    text: "Places",
                    url: "#",
                    current: false,
                },
                {
                    text: "Blog",
                    url: "#",
                    current: false,
                },
                {
                    text: "About",
                    url: "#",
                    current: false,
                },
                {
                    text: "Contact",
                    url: "#",
                    current: false,
                },
                
            ],
    }
  }, 
}
</script>

<style lang="scss">
@import "../assets/scss/partials/_variables.scss";

.footer {
  

  .center-footer {
    width: 80%;
    height: 200px;
    margin: 0 auto;
    display: flex;
    .img-footer {
      width: 25%;
      padding-right: 2em;
      border-right: 0.5px solid $silverChalice;
      display: flex;
      flex-direction: column;
      justify-content: center;
      img {
        padding-bottom: 1em;
      }
    }
  }

  .nav-footer {
    width: 25%;
    display: flex;
    align-items: center;
    border-right: 0.5px solid $silverChalice;
    ul {
      list-style: none;
      padding-left: 2em;
      li {
        a {
          text-decoration: none;
          color: $capeCod;
          font-family: $fontFamily;
          font-weight: bold;
          font-size: 0.5em;
        }
      }
    }
  }

  .contact {
    width: 25%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    border-right: 0.5px solid $silverChalice;
    #contact-title {
      font-family: $fontFamily;
      font-size: 0.6em;
      color: $orange;
      padding-left: 1em;
    }
    ul {
      list-style: none;
      li {
        display: flex;
        font-family: $fontFamily;
        font-size: 0.5em;
        color: $capeCod;
        padding: 1em; 
        p {
          padding-left: 0.5em;
        }
      }
    } 
  }

  .app {
    width: 25%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    padding-left: 1em;
    #app-title {
      font-family: $fontFamily;
      font-size: 0.6em;
      color: $orange;
      padding-bottom: 0.5em;
    }
    img {
      width: 75%;
      height: 20%;
      padding-bottom: 0.5em;
      cursor: pointer;
    }
  }

  .copyright {
    padding: 0.5em 0;
    margin-top: 2em;
    display: flex;
    align-items: center;
    background-color: $cararra;
    a {
      margin-right: 30%;
      margin-left: 1em;
    }
    .fa-chevron-up {
      width: 20px;
      height: 20px;
      background-color: $silverChalice;
      text-align: center;
      border-radius: 50%;
      
    }
    p {
      font-family: $fontFamily;
      font-size: 0.3em;
      color: $silverChalice;
    }
  }
}

</style>