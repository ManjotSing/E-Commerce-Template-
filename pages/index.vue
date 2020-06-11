<template>
  <div class="home">
      <NavBar />
      <Carousel />
      <hr />
      <Lotteries />
      <hr />
      <Footer />
  </div>
</template>

<script>
import NavBar from '~/components/NavBar.vue'
import Carousel from '~/components/Carousel.vue'
import Lotteries from '~/components/Lotteries.vue'
import Footer from '~/components/Footer.vue'
export default {
  components: {
    NavBar,
    Carousel,
    Lotteries,
    Footer
  }
}
</script>

<style>
</style>
