<template>
  <main>
    <Jumbotron />
    <PopularRecepies />
    <Collection />
    <FarmTable />
  </main>
</template>

<script>
import Jumbotron from './Jumbotron.vue'
import PopularRecepies from './PopularRecepies.vue'
import Collection from './Collection.vue'
import FarmTable from './FarmTable.vue'

export default {
    name: 'Main',
    components:{
      Jumbotron,
      PopularRecepies,
      Collection,
      FarmTable,
    }
}

</script>

<style lang="scss">
  @import "../assets/scss/partials/_variables.scss";

 
</style>