<template>
  <v-card fixed app style="z-index: 2">
    <v-toolbar class="teal darken-3" dense height="75px">
      <v-toolbar-title>
        <v-img
          :src="require('@/static/mainLogo_clear.png')"
          height="50px"
          width="200px"
          contain
        />
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-app-bar-nav-icon class="hidden-lg-and-up"></v-app-bar-nav-icon>
      <v-menu offset-y class="hidden-md-and-down">
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
    </v-toolbar>
  </v-card>
</template>

<script>
export default {
  data: () => ({
    items: [
      { title: 'Click me' },
      { title: 'Click me' },
      { title: 'Click me' },
      { title: 'Click me' }
    ]
  })
}
</script>
