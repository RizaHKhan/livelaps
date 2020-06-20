<template>
  <v-app id="inspire" dark>
    <Navigation />
    <v-carousel hide-delimiters cycle="true" :show-arrows="false" height="100%">
      <v-carousel-item
        v-for="(item, i) in items"
        :key="i"
        :src="item.src"
        transition="fade-transition"
      >
        <nuxt />
      </v-carousel-item>
      <Footer />
    </v-carousel>
  </v-app>
</template>

<script>
import Footer from '@/components/Footer'
import Navigation from '@/components/Navigation'

export default {
  components: {
    Footer,
    Navigation
  },
  data() {
    return {
      items: [
        { src: '/cover.jpg' },
        { src: '/cover10.jpg' },
        { src: '/cover12.jpg' },
        { src: '/cover3.jpg' },
        { src: '/cover5.jpg' },
        { src: '/cover6.jpg' },
        { src: '/cover7.jpg' },
        { src: '/cover8.jpg' },
        { src: '/cover9.jpg' },
        { src: '/cover11.jpg' }
      ]
    }
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
