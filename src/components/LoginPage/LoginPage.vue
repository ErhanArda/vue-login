<template>
  <v-container>
    <v-layout>
      <v-row class="mx-16 my-15">
                <v-col cols="12" md="1">
                </v-col>

        <v-col cols="12" md="5" style="border: 2px solid aqua">
          <v-card class="ma-auto" outlined max-width="550" style="border: 2px solid orange">
            <Login/>
          </v-card>
        </v-col>

        <v-col cols="12" md="5">
          <!-- <v-card class="mx-10 my-15"> -->
          <v-card class="ma-auto" outlined max-width="550" style="border: 2px solid blue">
            <Register />
          </v-card>
        </v-col>
        <v-col cols="12" md="1">
        </v-col>
      </v-row>
    </v-layout>
  </v-container>
</template>

<script>
import Login from "./Login/Login";
import Register from "./Register/Register";

export default {
  data: () => ({}),
  components: {
    Login,
    Register,
  },

  methods: {},
};
</script>
