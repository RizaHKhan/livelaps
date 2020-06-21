<template>
  <v-card fixed app style="z-index: 2">
    <v-toolbar class="teal darken-3" dense height="75px">
      <v-toolbar-title>
        <nuxt-link to="/">
          <v-img
            :src="require('@/static/mainLogo_clear.png')"
            height="50px"
            width="200px"
            contain
          />
        </nuxt-link>
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-app-bar-nav-icon class="hidden-lg-and-up" @click="drawer = !drawer">
      </v-app-bar-nav-icon>
      <div class="hidden-md-and-down">
        <v-menu offset-y>
          <template v-slot:activator="{ on, attrs }">
            <v-btn color="primary" dark v-bind="attrs" v-on="on">
              Dropdown
            </v-btn>
          </template>
          <v-list>
            <v-list-item v-for="(item, index) in items" :key="index">
              <v-list-item-title>{{ item.title }}</v-list-item-title>
            </v-list-item>
          </v-list>
        </v-menu>
      </div>
    </v-toolbar>
    <v-navigation-drawer
      v-model="drawer"
      absolute
      bottom
      temporary
      left
      width="400px"
    >
      <v-list nav dense>
        <v-list-item v-for="item in items" :key="item.title">
          <v-list-item-title>{{ item.title }}</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
  </v-card>
</template>

<script>
export default {
  data() {
    return {
      drawer: false,
      items: [
        { title: 'Click me' },
        { title: 'Click me' },
        { title: 'Click me' },
        { title: 'Click me' }
      ]
    }
  }
}
</script>
