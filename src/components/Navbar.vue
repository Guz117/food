<template>
  <div class="navbar">
      <div class="nav-avada">
        <img :src="require('../assets/images/avada-food-logo.png')" alt="">
      </div>
      <ul class="ul-navbar">
          <li v-for="(linkNav, index) in linksNav"
          :key="index"
          @click="changeActive(index)"
          ><a :class="(linkNav.current == true) ? 'active' : ''" 
          :href="linkNav.url">{{ linkNav.text }}</a></li>
          <li><i class="fas fa-search"></i></li>
      </ul>
  </div>
</template>

<script>
export default {
    name: 'Navbar',
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
   methods: {
    changeActive(indexElement) {
       this.linksNav.forEach(
        (element, index) => {
          if (index === indexElement) {
            element.current = true;
          } else {
            element.current = false;
          }
        }
      )
    }
  }
    
}
</script>

<style lang="scss">
@import "../assets/scss/partials/_variables.scss";

    .navbar {
        width: 80%;
        margin: 0 auto;
    }

    .nav-avada {
        display: flex;
        justify-content: center;
        padding-top: 2em;
    }

    .ul-navbar {
        display: flex;
        justify-content: center;
        list-style: none;
        padding: 2em 0;
        li {
            font-size: 0.8em;
            font-weight: bold;
            padding: 0 2em;
            a {
                text-decoration: none;
                font-family: $fontFamily;
                color: $shark;
                padding-bottom: 0.7em;
                &:hover,
                &:active,
                &.active {
                    color: $orange;
                    border-bottom: 3px solid $orange;
                }
            }
        }
    }
</style>