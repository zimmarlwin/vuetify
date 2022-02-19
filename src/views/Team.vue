<template>
  <div>
    <h1 class="subheading grey--text">Team</h1>
    <v-container class="my-5">
      <v-layout row wrap>
        <v-flex xs12 sm6 md4 lg3 v-for="person in team" :key="person.name">
          <v-card depressed class="text-center ma-3">
            <v-responsive class="pt-4">
              <v-avatar size="100" class="grey lighten-2">
                <img :src="person.avatar" alt="" />
              </v-avatar>
            </v-responsive>
            <v-card-text>
              <div class="subheading">{{ person.name }}</div>
              <div class="grey--text">{{ person.role }}</div>
            </v-card-text>
            <v-card-actions>
              <v-btn text clor="grey">
                <v-icon small left>message</v-icon>
                <span>Message</span>
              </v-btn>
            </v-card-actions>
          </v-card>
        </v-flex>
      </v-layout>
    </v-container>
  </div>
</template>

<script>
export default {
  name: "Team",
  data() {
    return {
      team: [
        {
          name: "The Net Nija",
          role: "Web Developer",
          avatar: "/images/avater_1.png",
        },
        {
          name: "Ryu",
          role: "Graphic designer",
          avatar: "/images/avater_2.png",
        },
        {
          name: "Cju Li",
          role: "Web Developer",
          avatar: "/images/avater_3.png",
        },
        {
          name: "Gougen",
          role: "Social media mavericke",
          avatar: "/images/avater_4.png",
        },
        { name: "Yochi", role: "Sales guru", avatar: "/images/avater_5.png" },
      ],
    };
  },
};
</script>

<style scoped>
</style>