<template>
  <div>
    <v-dialog max-width="600px" v-model="dialog" hide-overlay transition="">
      <template v-slot:activator="{ on, attrs }">
        <v-btn color="primary" dark v-bind="attrs" v-on="on" class="success">
          Add New Project
        </v-btn>
      </template>
      <v-card>
        <v-card-title><h2>Add New Project</h2></v-card-title>
        <v-card-text>
          <v-form class="px-2">
            <v-text-field
              label="Title"
              v-model="title"
              prepend-icon="folder"
            ></v-text-field>
            <v-textarea
              label="Information"
              v-model="content"
              prepend-icon="edit"
            ></v-textarea>
            <v-menu>
              <template v-slot:activator="{ on, attrs }">
                <v-text-field
                  :value="computedDateFormattedDatefns"
                  v-bind="attrs"
                  v-on="on"
                  label="Due dates"
                  prepend-icon="date_range"
                  @click:clear="date = null"
                ></v-text-field>
              </template>
              <v-date-picker
                v-model="due"
                @change="menu2 = false"
              ></v-date-picker>
            </v-menu>
            <v-btn depressed class="success" @click="submit"
              >Add Project
            </v-btn>
          </v-form>
        </v-card-text>
      </v-card>
    </v-dialog>
  </div>
</template>

<script>
import { format, parseISO } from "date-fns";
export default {
  data() {
    return {
      title: "",
      content: "",
      due: "",
    };
  },
  methods: {
    submit() {
      console.log(this.title, this.content, this.due);
    },
  },
  computed: {
    computedDateFormattedDatefns() {
      return this.due ? format(parseISO(this.due), "Do MMM YYY") : "";
    },
  },
};
</script>

<style scoped>
</style>