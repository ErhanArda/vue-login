<template>
  <v-app>
    <v-app-bar app color="primary" dark>
      <v-icon>mdi-code-tags</v-icon>
      <v-spacer></v-spacer>

      <Navigation />
      <!-- <v-btn
        href="https://github.com/vuetifyjs/vuetify/releases/latest"
        target="_blank"
        text
      >
        <span class="mr-2">s Release</span>
        <v-icon>mdi-open-in-new</v-icon>
      </v-btn> -->
    </v-app-bar>
    <v-content>
      <router-view></router-view>
    </v-content>
  </v-app>
</template>

<script>
// import LoginPage from "./components/LoginPage/LoginPage";
import Login from "./views/Login";
import Navigation from "./components/Navigation/Navigation";
export default {
  name: "App",

  components: {
    // LoginPage,
    Login,
    Navigation,
  },

  data: () => ({
    //
  }),
};
</script>
