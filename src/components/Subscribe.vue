<template>
  <div class="subscribe">
    <div class="subscribe-center">
      <h4>Subscribe Receive A Free eBook</h4>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptates omnis distinctio doloribus harum sunt explicabo nobis numquam soluta</p>
      <div class="email">
        <form action="">
          <label for="insert"></label>
          <input id="insert" type="text" placeholder="Insert your email_*">
        </form>
        <button>SUBSCRIBE</button>
      </div>
      <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Consequat</p>
    </div>

  </div>
</template>

<script>
export default {
    name: 'Subscribe'
}
</script>

<style lang="scss">
@import "../assets/scss/partials/_variables.scss";

.subscribe {
  width: 100%;
  height: 300px;
  background: url('../assets/images/subscribe-sec-bg.png');
  background-size: cover;
  display: flex;
  justify-content: center;
  align-items: center;

  .subscribe-center {
    width: 60%;
    h4 {
      text-align: center;
    }
    p {
      text-align: center;
      font-family: $fontFamily;
      font-size: 0.7em;
      line-height: 2em;
      color: $nevada;
    }  

    .email {
      padding-top: 1em;
      display: flex;
      justify-content: center;
      input {
        width: 300px;
        font-size: 0.6em;
        padding: 0.4em;
      }
      button {
        border: 0;
        background-color: $orange;
        color: white;
        margin-left: 1em;
        padding: 0 1em;
        cursor: pointer;
      }
    }
    p {
      padding-top: 1em;
    }
  }
}

</style>