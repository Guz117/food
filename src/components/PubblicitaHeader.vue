<template>
  <div class="pubblicita">
      <div>
          <ul class="ul-pubblicita">
              <li class="pubb download"><a href="#">Download App</a></li>
              <li class="pubb ios"><a href="#">iOS</a></li>
              <li class="pubb advertise"><a href="#">Advertise with us</a></li>
          </ul>
      </div>
      <div>
          <ul class="ul-social">
              <li class="social"><a href="#"><i class="fab fa-facebook-f"></i></a></li>
              <li class="social"><a href="#"><i class="fab fa-instagram"></i></a></li>
              <li class="social"><a href="#"><i class="fab fa-twitter"></i></a></li>
              <li class="social"><a href="#"><i class="fab fa-youtube"></i></a></li>
          </ul>
      </div>
  </div>
</template>

<script>
export default {
    name: 'PubblicitaHeader'
}
</script>

<style lang="scss">
@import "../assets/scss/partials/_variables.scss";

    .pubblicita {
        display: flex;
        justify-content: space-between;
        width: 80%;
        margin: 0 auto;
        padding-top: 0.5em;
    }

    .ul-pubblicita, .ul-social {
        display: flex;
        list-style: none;
        padding-left: 0;
        a {
            text-decoration: none;
            color: $silverChalice;
        }
    }

    .pubb {
        font-size: 0.8em;
        font-family: $fontFamily;
    }
    .download {
        padding-right: 0.5em;
    }

    .ios {
        padding: 0 1px;
        background-color: $orange;
        border-radius: 2px;
        a {
            color: $springWood
        }
    }

    .advertise {
        padding-left: 1.5em;
    }

    .social {
        font-size: 0.8em;
        padding-left: 1em;
    }
</style>