<template>
  <v-carousel
    hide-delimiters
    cycle="true"
    absolute
    :show-arrows="false"
    height="100%"
    transition="fade-transition"
  >
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
</template>

<script>
export default {
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
.v-carousel {
  position: absolute;
}
</style>
