<template>
  <v-container>
    <v-layout align-center justify-center>
      <v-flex xs12 sm8 md8 lg8>
        <div class="mx-auto my-15">
          <div class="text-center">
            <div>
              <h4 class="display-1">Henüz Üye Değil Misiniz?</h4>
            </div>

            <div class="mt-8 mb-10">
              <p class="body-2">
                Üyelerimize özel hizmetlerimizden faydalanabilmek için üye olun.
              </p>
            </div>

            <v-card-actions>
              <v-spacer></v-spacer>
              <v-btn outlined block color="primary" to="/signup">Hemen Üye Ol</v-btn>
            </v-card-actions>
          </div>
        </div>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {};
</script>
