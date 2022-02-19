<template>
  <div class="projects">
    <h1 class="subheading grey--text">Projects</h1>

    <v-container class="my-5">
      <v-expansion-panels>
        <v-expansion-panel v-for="(project, i) in projects" :key="i">
          <v-expansion-panel-header>
            {{ project.title }}</v-expansion-panel-header
          >
          <v-expansion-panel-content>
            <v-card>
              <v-card-text class="px-4 grey--text">
                <div class="font-weight-bold">due bye {{ project.due }}</div>
                <div>{{ project.content }}</div>
              </v-card-text>
            </v-card>
          </v-expansion-panel-content>
        </v-expansion-panel>
      </v-expansion-panels>
    </v-container>
  </div>
</template>

<script>
export default {
  name: "Projects",
  data() {
    return {
      projects: [
        {
          title: "Design a new website1",
          person: "The Net Ninga",
          due: "1st Jan 2019",
          status: "complete",
          content:
            "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Tenetur, sed animi quasi similique incidunt iure. Suscipit nisi iusto pariatur ut sint, quod, odio doloribus commodi assumenda exercitationem quis repellat obcaecati!",
        },
        {
          title: "Design a new website2",
          person: "Ryu",
          due: "1st Feb 2019",
          status: "ongoing",
          content:
            "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Tenetur, sed animi quasi similique incidunt iure. Suscipit nisi iusto pariatur ut sint, quod, odio doloribus commodi assumenda exercitationem quis repellat obcaecati!",
        },
        {
          title: "Design a new website3",
          person: "Cju Li",
          due: "1st March 2019",
          status: "overdue",
          content:
            "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Tenetur, sed animi quasi similique incidunt iure. Suscipit nisi iusto pariatur ut sint, quod, odio doloribus commodi assumenda exercitationem quis repellat obcaecati!",
        },
        {
          title: "Design a new website4",
          person: "Gougen",
          due: "1st April 2019",
          status: "ongoing",
          content:
            "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Tenetur, sed animi quasi similique incidunt iure. Suscipit nisi iusto pariatur ut sint, quod, odio doloribus commodi assumenda exercitationem quis repellat obcaecati!",
        },
        {
          title: "Design a new website5",
          person: "Yochi",
          due: "1st May 2019",
          status: "complete",
          content:
            "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Tenetur, sed animi quasi similique incidunt iure. Suscipit nisi iusto pariatur ut sint, quod, odio doloribus commodi assumenda exercitationem quis repellat obcaecati!",
        },
      ],
    };
  },
};
</script>

<style scoped>
</style>



