<template>
  <v-app id="inspire" dark>
    <Carousel />
    <Navigation />
    <nuxt />
    <Footer />
  </v-app>
</template>

<script>
import Footer from '@/components/Footer'
import Navigation from '@/components/Navigation'
import Carousel from '@/components/Carousel'

export default {
  components: {
    Footer,
    Navigation,
    Carousel
  }
}
</script>

<style lang="scss" scoped>
html {
  overflow: hidden;
}

#inspire {
  height: 100vh;
  background-color: black;
  border-style: solid;
  border-color: grey;
}
</style>
