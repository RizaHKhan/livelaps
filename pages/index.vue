<template>
  <v-container fluid>
    <v-container
      style="position: relative; 
      z-index: 2; 
      height: 100vh;
      display: flex; 
      align-items: center"
    >
      <v-row class="my-auto">
        <v-col class="ma-auto">
          <h1 class="display-4 font-weight-thin">Hello World</h1>
          <p class="display-1 font-weight-thin">Some other text</p>
          <v-row>
            <v-col cols="12" md="6" lg="4">
              <v-btn
                v-for="button in buttons"
                :key="button.id"
                :to="button.link"
                class="blue ma-1"
              >
                {{ button.name }}
              </v-btn>
            </v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-container>
    <v-carousel
      height="100%"
      cycle="true"
      :show-arrows="false"
      :hide-delimiters="true"
      transition="transition-fast-in-fast-out"
      class="absolute"
    >
      <v-carousel-item
        v-for="item in items"
        :key="item.src"
        :src="item.src"
      ></v-carousel-item>
    </v-carousel>
  </v-container>
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
      ],
      buttons: [
        { id: 1, name: 'Button 1', link: '/home' },
        { id: 1, name: 'Button 1', link: '/' },
        { id: 1, name: 'Button 1', link: '/' },
        { id: 1, name: 'Button 1', link: '/' },
        { id: 1, name: 'Button 1', link: '/' },
        { id: 1, name: 'Button 1', link: '/' },
        { id: 1, name: 'Button 1', link: '/' }
      ]
    }
  }
}
</script>

<style scoped lang="scss">
.absolute {
  top: 0;
  position: absolute;
  z-index: 0;
}
</style>
