<template>
  <v-card color="grey lighten-4" flat height="200px" tile>
    <v-toolbar dense>
      <v-app-bar-nav-icon></v-app-bar-nav-icon>

      <v-toolbar-title>
        <v-img
          :src="require('@/static/mainLogo_clear.png')"
          height="50px"
          width="100px"
        />
      </v-toolbar-title>

      <v-spacer></v-spacer>
    </v-toolbar>
  </v-card>
</template>

<script>
export default {
  data: () => ({})
}
</script>
