<template>
  <main>
    <Jumbotron />
    <PopularRecepies />
    <Collection />
   
  </main>
</template>

<script>
import Jumbotron from './Jumbotron.vue'
import PopularRecepies from './PopularRecepies.vue'
import Collection from './Collection.vue'

export default {
    name: 'Main',
    components:{
      Jumbotron,
      PopularRecepies,
      Collection,
    }
}

</script>

<style lang="scss">
  @import "../assets/scss/partials/_variables.scss";

 
</style>