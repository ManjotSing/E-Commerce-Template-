<template>
  <div class="home">
      <NavBar />
      <Carousel />
      <Lotteries />
  </div>
</template>

<script>
import NavBar from '~/components/NavBar.vue'
import Carousel from '~/components/Carousel.vue'
import Lotteries from '~/components/Lotteries.vue'
export default {
  components: {
    NavBar,
    Carousel,
    Lotteries
  }
}
</script>

<style>
</style>
