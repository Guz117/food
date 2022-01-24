<template>
  <div>
      <PubblicitaHeader />
      <Navbar />
  </div>
</template>

<script>
import PubblicitaHeader from './PubblicitaHeader.vue'
import Navbar from './Navbar.vue'

export default {
    name: 'Header',
    components: {
        PubblicitaHeader,
        Navbar,
    },
    
}
</script>

<style lang="scss">

</style>