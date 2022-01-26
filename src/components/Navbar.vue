<template>
  <div class="navbar">
      <div class="nav-avada">
        <img :src="require('../assets/images/avada-food-logo.png')" alt="">
      </div>
      <i class="fas fa-bars" v-on:click="isActive = !isActive"></i>
      <ul class="ul-navbar">
          <li v-for="(linkNav, index) in linksNav"
          :key="index"
          @click="changeActive(index)"
          ><a :class="(linkNav.current == true) ? 'active' : ''" 
          :href="linkNav.url">{{ linkNav.text }}</a></li>
          <li><i class="fas fa-search"></i></li>
      </ul>
      <div class="hamburger-menu" v-bind:class="{ active: isActive }">
        <ul class="hamburger-navbar">
          <li v-for="(linkNav, index) in linksNav"
          :key="index"
          @click="changeActive(index)"
          ><a :class="(linkNav.current == true) ? 'active' : ''" 
          :href="linkNav.url">{{ linkNav.text }}</a></li>
          <li><i class="fas fa-search"></i></li>
        </ul>
        <a href="#" class="close">
          <i class="fas fa-times" v-on:click="isActive = !isActive"></i>
        </a>
      </div>
  </div>
</template>

<script>
export default {
    name: 'Navbar',
    data() { 
    return {
      isActive: false,
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
    },
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
        .fa-bars {
          font-size: 2em;
          padding: 0.5em 0;
          display: none;
        }

        .hamburger-menu {
          position: absolute;
          top: 0;
          left: 0;
          display: none;
          padding: 20px;
          width: 100%;
          height: 100%;
          min-width: 100vw;
          min-height: 100vh;
          background: white;

        .fa-search {
          color: $shark;
        }

        .fa-search:hover {
          color: $orange;
        }

      }
      .hamburger-menu ul {
          display: flex;
          height: 100%;
          flex-direction: column;
          align-items: flex-start;
          list-style: none;
          li {
            padding-bottom: 1em;
          }
          a:hover {
            color: $orange;
          }
      }
      .hamburger-menu ul li a {
          color: $shark;
          text-decoration: none;
          font-size: 1em;
          font-family: $fontFamily;
          
      }
      .close {
          display: block;
          position: absolute;
          right: 20px;
          top: 20px;
          color: $orange;
          font-size: 35px;
          text-decoration: none;
      }

@media screen and (max-width: 730px)
{
    .ul-navbar {
        display: none;
    }
    .fa-bars {
        display: block;
        height: 100%;
        line-height: 70px;
        font-size: 20px;
    }

    .hamburger-menu.active {
        display: block;
    }
}
</style>