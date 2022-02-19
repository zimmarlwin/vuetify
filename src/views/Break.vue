<template>
  <div>
    <h1>Breakpoints and Visibility</h1>
    <v-btn class="hidden-md-and-down">Hide Large Tablet and Down</v-btn
    ><br /><br />
    <v-btn class="hidden-md-and-up">Hide Large Tablet and Up</v-btn><br /><br />
    <v-btn class="hidden-sm-only">Small to Medium Tablet Only Hide</v-btn>
  </div>
</template>

<script>
export default {
  name: "Break",
};
</script>

<style scoped>
</style>