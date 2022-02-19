<template>
  <div>
    <h1 class="subheading grey--text">Dashboard</h1>
    <v-container class="my-5">
      <v-layout row class="mb-6">
        <v-tooltip top>
          <template v-slot:activator="{ on: tooltip }">
            <v-btn
              small
              text
              color="grey"
              @click="sortBy('title')"
              v-bind="attrs"
              v-on="{ ...tooltip, ...menu }"
            >
              <v-icon left small>folder</v-icon>
              <span class="caption text-lowercase">By project name</span>
            </v-btn>
          </template>
          <span>Sort projects by porjects name</span>
        </v-tooltip>
        <v-tooltip top>
          <template v-slot:activator="{ on: tooltip }">
            <v-btn
              small
              text
              color="grey"
              @click="sortBy('title')"
              v-bind="attrs"
              v-on="{ ...tooltip, ...menu }"
            >
              <v-icon left small>person</v-icon>
              <span class="caption text-lowercase">By person</span>
            </v-btn>
          </template>
          <span>Sort projects by person</span>
        </v-tooltip>
      </v-layout>

      <v-card tile v-for="project in projects" :key="project.title">
        <v-layout row wrap :class="`pa-4 project ${project.status}`">
          <v-flex xs12 md6>
            <div class="caption grey--text">Project Title</div>
            <div>{{ project.title }}</div>
          </v-flex>
          <v-flex xs6 sm4 md2>
            <div class="caption grey--text">Person</div>
            <div>{{ project.person }}</div>
          </v-flex>
          <v-flex xs6 sm4 md2>
            <div class="caption grey--text">Due by</div>
            <div>{{ project.due }}</div>
          </v-flex>
          <v-flex xs6 sm4 md2>
            <div class="text-right mr-4">
              <v-chip
                small
                :class="`${project.status} white--text caption my-2`"
                >{{ project.status }}</v-chip
              >
            </div>
          </v-flex>
        </v-layout>
      </v-card>

      <v-divider></v-divider>
    </v-container>
  </div>
</template>


<script>
export default {
  name: "Home",
  data() {
    return {
      projects: [
        {
          title: "Ahis is Title",
          person: "This is person",
          due: "1st Jan 2019",
          status: "overdue",
        },
        {
          title: "Dhis is Title2",
          person: "This is person2",
          due: "1st Jan 20192",
          status: "ongoing",
        },
        {
          title: "Bhis is Title3",
          person: "This is person3",
          due: "1st Jan 20193",
          status: "ongoing",
        },
        {
          title: "Ehis is Title4",
          person: "This is person4",
          due: "1st Jan 20194",
          status: "complete",
        },
      ],
    };
  },
  method: {
    sortBy(prop) {
      this.projects.sort((a, b) => (a[prop] < b[prop] ? -1 : 1));
    },
  },
};
</script>


<style scoped>
.project.complete {
  border-left: 4px solid #f07109;
}
.project.ongoing {
  border-left: 4px solid #4dd13c;
}
.project.overdue {
  border-left: 4px solid #d13c75;
}
.theme--light.v-chip.complete {
  background: #faa22c;
}
.theme--light.v-chip.ongoing {
  background: #0eb329;
}
.theme--light.v-chip.overdue {
  background: #be0e58;
}
</style>
