<template>
  <v-app class="grey lighten-4">
    <Navbar />
    <v-main class="mx-4 mt-2">
      <router-view />
    </v-main>
  </v-app>
</template>


<script>
import Navbar from "./components/Navbar.vue";
export default {
  components: { Navbar },
  name: "App",
  data: () => ({
    //
  }),
};
</script>
