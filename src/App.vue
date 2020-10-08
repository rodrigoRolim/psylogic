<template>
  <v-app>
    <v-app-bar
      app
      color="primary"
      dark
    >
      <v-img
        class="mx-2"
        :src="require('./assets/logoPsy.png')"
        max-height="300"
        max-width="280"
        contain
      ></v-img>
    </v-app-bar>

    <v-main>
      <router-view></router-view>
    </v-main>
  </v-app>
</template>

<script>

export default {
  name: 'App',

  components: {
  },

  data: () => ({
    //
  }),
};
</script>
