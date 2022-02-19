<template>
  <div class="home">
    <h1>Homepage</h1>
    <v-btn class="pink white--text">click me</v-btn><br /><br />
    <!-- dark is props -->
    <v-btn dark color="pink">Pink Background and font bold</v-btn><br /><br />
    <v-btn depressed color="pink">Depressed (Sharp Border)</v-btn><br /><br />
    <v-btn text color="pink">Flat ( Make Transparency Background)</v-btn
    ><br /><br />
    <v-btn depressed class="pink white--text">
      <v-icon left>email</v-icon>
      <span>email me</span> </v-btn
    ><br /><br />
    <v-btn depressed small class="pink white--text">
      <v-icon left>email</v-icon>
      <span>email me</span> </v-btn
    ><br /><br />
    <v-btn depressed large class="pink white--text">
      <span>email me</span>
      <v-icon right>email</v-icon> </v-btn
    ><br /><br />
    <v-btn fab depressed small dark class="purple">
      <v-icon>favorite</v-icon>
    </v-btn>
  </div>
</template>

<script>
export default {
  name: "Button",
};
</script>

<style scoped>
</style>