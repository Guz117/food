<template>
  <main>
    <Jumbotron />
    <!-- <FoodieJournal /> -->
  </main>
</template>

<script>
import Jumbotron from './Jumbotron.vue'
// import FoodieJournal from './FoodieJournal.vue'

export default {
    name: 'Main',
    components:{
      Jumbotron,
      // FoodieJournal,
    }
}

</script>

<style lang="scss">
  @import "../assets/scss/partials/_variables.scss";

 
</style>