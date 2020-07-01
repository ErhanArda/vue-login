<template>
    <v-form ref="form" v-model="valid" lazy-validation>
            <v-radio-group v-model="row" row>
      <v-radio label="Bireysel Üyelik" value="radio-1"></v-radio>
      <v-radio label="Kurumsal Üyelik" value="radio-2"></v-radio>
    </v-radio-group>
        <v-row>
            <v-col cols="12" md="6"
                ><v-text-field
                v-model="name"
                :rules="nameRules"
                label="Name"
                outlined
                dense
                required
                ></v-text-field>
            </v-col>
            <v-col cols="12" md="6">
            <v-text-field
                v-model="SurName"
                :rules="SurNameRules"
                label="Soyadınız"
                outlined
                dense
                required
                ></v-text-field>
        </v-col>
        </v-row>
          <v-text-field
            v-model="email"
            :rules="emailRules"
            label="E-mail"
            outlined
            dense
            required
            ></v-text-field>
            <v-text-field
                name="password"
                label="Şifre"
                id="password"
                :type="value ? 'password' : 'text'"
                v-model="password"
                :rules="passwordRules"
                outlined
                dense
                required
                @click:append="() => (value = !value)"
                :append-icon="value ? 'mdi-eye' : 'mdi-eye-off'"
              ></v-text-field>
        <v-select
        v-model="select"
        :items="items"
        :rules="[(v) => !!v || 'Item is required']"
        label="Item"
        outlined
        dense
        required
        ></v-select>

        <v-checkbox
        v-model="checkbox"
        :rules="[(v) => !!v || 'You must agree to continue!']"
        label="Do you agree?"
        required
        ></v-checkbox>


        <v-btn color="error" class="mr-4" @click="reset">
        Reset Form
        </v-btn>

        <v-btn color="warning" @click="resetValidation">
        Reset Validation
        </v-btn>
    </v-form>
</template>

<script>
export default {
  data: () => ({
    valid: true,
    name: "",
    surName:"",
    password:null,
    radios: 'radio-1',

    nameRules: [
      (v) => !!v || "Name is required",
      (v) => (v && v.length <= 10) || "Name must be less than 10 characters",
    ],
    SurNameRules: [
      (v) => !!v || "Surname is required",
      (v) => (v && v.length <= 10) || "Name must be less than 10 characters",
    ],
    email: "",
    emailRules: [
      (v) => !!v || "E-mail is required",
      (v) => /.+@.+\..+/.test(v) || "E-mail must be valid",
    ],
    passwordRules: [
      (v) => !!v || "Password is required",
      (v) => (v && v.length >= 5) || "Password must have 5+ characters",
    ],
    select: null,
    items: ["Item 1", "Item 2", "Item 3", "Item 4"],
    checkbox: false,
  }),

  methods: {
    // validate() {
    //   this.$refs.form.validate();
    // },
    reset() {
      this.$refs.form.reset();
    },
    resetValidation() {
      this.$refs.form.resetValidation();
    },
  },
};
</script>
