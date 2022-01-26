<template>
  <main>
    <Jumbotron />
    <PopularRecipes />
    <Collection />
    <FarmTable />
    <Subscribe />
    <EndMain />
  </main>
</template>

<script>
import Jumbotron from './Jumbotron.vue'
import PopularRecipes from './PopularRecipes.vue'
import Collection from './Collection.vue'
import FarmTable from './FarmTable.vue'
import Subscribe from './Subscribe.vue'
import EndMain from './EndMain.vue'

export default {
    name: 'Main',
    components:{
      Jumbotron,
      PopularRecipes,
      Collection,
      FarmTable,
      Subscribe,
      EndMain,
    }
}

</script>

<style lang="scss">
  @import "../assets/scss/partials/_variables.scss";

 
</style>