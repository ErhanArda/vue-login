<template>
  <v-app>
    <v-app-bar app color="primary" dark> </v-app-bar>
    <v-content>
      <Login />
    </v-content>
  </v-app>
</template>

<script>
// import LoginPage from "./components/LoginPage/LoginPage";
import Login from "./views/Login"

export default {
  name: "App",

  components: {
    // LoginPage,
    Login
  },

  data: () => ({
    //
  }),
};
</script>
