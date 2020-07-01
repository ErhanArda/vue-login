<template>
  <v-container>
    <v-layout>
      <v-card
        class="ma-auto"
        outlined
        max-width="80%"
        style="border: 2px solid orange"
      >
        <v-row class="mx-16 my-15">

          <v-col cols="12" md="6" style="border: 2px solid aqua">
              <Left/>
              <!-- <Login /> -->
          </v-col>
          <v-col cols="12" md="2"></v-col>

          <v-col cols="12" md="4">
            <v-sheet elevation="12" class="pa-12">
              <v-textarea
                v-model="model"
                :auto-grow="autoGrow"
                :clearable="clearable"
                :counter="counter ? counter : false"
                :filled="filled"
                :flat="flat"
                :hint="hint"
                :label="label"
                :loading="loading"
                :no-resize="noResize"
                :outlined="outlined"
                :persistent-hint="persistentHint"
                :placeholder="placeholder"
                :rounded="rounded"
                :row-height="rowHeight"
                :rows="rows"
                :shaped="shaped"
                :single-line="singleLine"
                :solo="solo"
              ></v-textarea>
              <div class="mt-12 text-center">Value: {{ model }}</div>
            </v-sheet>
          </v-col>
          <v-col cols="12" md="1"> </v-col>
        </v-row>
      </v-card>
    </v-layout>
  </v-container>
</template>

<script>
// import Login from "../LoginPage/Login/Login";
import Left from "./SignUp/Left"

export default {
  data: () => ({}),
  components: {
    // Login,
    Left
  },

  methods: {},
};
</script>
