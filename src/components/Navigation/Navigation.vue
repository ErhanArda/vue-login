<template>
  <div>
    <nav>
      <router-link
        class="mr-5"
        v-for="routes in links"
        v-bind:key="routes.id"
        :to="`${routes.page}`"
      >
        <nav-title>
          <v-btn text>
            {{ routes.text }}
          </v-btn>
        </nav-title>
      </router-link>
    </nav>
  </div>
</template>

<script>
export default {
  data() {
    return {
      links: [
        {
          id: 0,
          text: "Home",
          page: "/",
        },
        {
          id: 1,
          text: "Login",
          page: "/login",
        },
        {
          id: 2,
          text: "SignUp",
          page: "/signup",
        },
      ],
    };
  },
};
</script>

<style>
.spacing {
  margin-right: 20px;
}
</style>
