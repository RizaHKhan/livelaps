<template>
  <v-app id="inspire" dark>
    <v-container fluid>
      <Navigation />
      <nuxt />
      <Footer />
    </v-container>
  </v-app>
</template>

<script>
import Footer from '@/components/Footer'
import Navigation from '@/components/Navigation'

export default {
  components: {
    Footer,
    Navigation
  }
}
</script>

<style>
html {
  overflow: hidden;
}

.container {
  overflow: hidden;
  padding: 0;
}

#inspire {
  border: none;
  height: 100vh;
}
</style>
