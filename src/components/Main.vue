<template>
  <main>
    <Jumbotron />
    <PopularRecepies />
   
  </main>
</template>

<script>
import Jumbotron from './Jumbotron.vue'
import PopularRecepies from './PopularRecepies.vue'

export default {
    name: 'Main',
    components:{
      Jumbotron,
      PopularRecepies,
    }
}

</script>

<style lang="scss">
  @import "../assets/scss/partials/_variables.scss";

 
</style>