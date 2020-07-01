<template>
  <v-container>
    <v-layout align-center justify-center>
      <v-flex xs12 md10>
        <div class="text-center">
          <div class="col-md-12 mt-5">
            <h4>ÜYE GİRİŞİ</h4>
          </div>
          <v-card-text>
            <v-form v-model="isValid">
              <v-text-field
                prepend-icon="mdi-account"
                name="login"
                label="E-posta"
                type="text"
                v-model="email"
                :rules="emailRules"
                outlined
                dense
                required
              ></v-text-field>
              <!-- <v-btn small right>şifremi unuttum</v-btn> -->
              <v-text-field
                prepend-icon="mdi-lock"
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
            </v-form>
          </v-card-text>
          <v-card-actions>
            <!-- <v-btn color="primary" :disabled="!isValid">Login</v-btn> -->
            <v-btn block color="primary" :disabled="!isValid" medium
              >Giriş Yap ve Devam Et</v-btn
            >
          </v-card-actions>

          <v-checkbox
            v-model="checkbox"
            :error-messages="checkboxErrors"
            label="Oturumumu sürekli açık tut"
            required
            @change="$v.checkbox.$touch()"
            @blur="$v.checkbox.$touch()"
          ></v-checkbox>

          <v-card-actions>
            <!-- <v-btn color="primary" :disabled="!isValid">Login</v-btn> -->
            <v-btn block color="red" outlined medium
              >Google ile Giriş Yap</v-btn
            >
          </v-card-actions>
          <v-card-actions>
            <!-- <v-btn color="primary" :disabled="!isValid">Login</v-btn> -->
            <v-btn block color="primary" outlined medium
              >Facebook ile Giriş Yap</v-btn
            >
          </v-card-actions>
        </div>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    email: null,
    password: null,
    isValid: true,
    value: true,
    checkbox: false,

    required: (value) => !!value || "Required.",

    emailRules: [
      (v) => !!v || "Email is required",
      (v) => /.+@.+/.test(v) || "E-mail must be valid",
    ],
    passwordRules: [
      (v) => !!v || "Password is required",
      (v) => (v && v.length >= 5) || "Password must have 5+ characters",
    ],
  }),

  methods: {},
};
</script>

<style>
.v-text-field {
  width: 500px;
}
</style>
