<template>
  <v-container>
    <v-row>
      <v-col cols="10">
        <div style="max-width: 60em" class="border py-5">
          <v-row>
            <v-col cols="2" class="mt-5 text-center"> 対象年度 </v-col>
            <v-col cols="3">
              <v-menu offset-y>
                <template v-slot:activator="{ on, attrs }">
                  <v-select
                    :items="sampleItems"
                    v-bind="attrs"
                    v-on="on"
                  ></v-select>
                </template>
              </v-menu>
              <v-card flat>
                <v-card-text> </v-card-text>
              </v-card>
            </v-col>
            <v-col cols="3">
              <v-text-field></v-text-field>
            </v-col>
            <v-col cols="3">
              <v-btn color="primary" depressed rounded>年度追加</v-btn>
            </v-col>
          </v-row>

          <v-row>
            <v-col cols="5">
              <v-card outlined class="fill-height">
                <v-card-title>{{ title }}</v-card-title>
                <v-data-table
                  :headers="sampleTableHeaders"
                  :items="sampleTable1Items"
                  show-select
                  disable-sort
                  hide-default-footer
                  dense
                ></v-data-table>
              </v-card>
            </v-col>
            <v-col cols="1" class="d-flex flex-column justify-center">
              <v-btn depressed class="mb-3"
                ><v-icon>mdi-arrow-left</v-icon></v-btn
              >
              <v-btn depressed><v-icon>mdi-arrow-right</v-icon></v-btn>
            </v-col>
            <v-col cols="5">
              <v-card outlined class="fill-height">
                <v-card-title>{{ titleRight }}</v-card-title>
                <v-data-table
                  :headers="sampleTableHeaders"
                  :items="sampleTable2Items"
                  show-select
                  disable-sort
                  hide-default-footer
                  dense
                ></v-data-table>
              </v-card>
            </v-col>
          </v-row>

          <v-row>
            <v-col class="col-10">
              <v-btn color="primary" depressed rounded class="mr-3">登録</v-btn>
              <v-btn depressed rounded class="mr-3">キャンセル</v-btn>
              <v-btn color="primary" depressed rounded>終了</v-btn>
            </v-col>
          </v-row>
        </div>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "Form",
  data() {
    return {
      title: "出身塾年度一覧",
      titleRight: "出身塾一覧",

      sampleItems: ["項目その1", "項目その2", "項目その3", "項目その4"],
      sampleTableHeaders: [
        { text: "学籍番号", value: "id", width: "100", class: "pt-6" },
        { text: "名前", value: "name", class: "pt-6" },
      ],
      sampleTable1Items: [
        { id: "002300011", name: "原田 尚子" },
        { id: "002300012", name: "真尾 光" },
        { id: "002300013", name: "丸山 久恵" },
        { id: "002300014", name: "森本 菜央" },
        { id: "002300015", name: "横野 堅大" },
      ],
      sampleTable2Items: [
        { id: "003500011", name: "吉澤 侑里" },
        { id: "003500012", name: "昆野 正照" },
        { id: "003500013", name: "張 楫" },
        { id: "003500014", name: "安田 起" },
      ],
    };
  },
};
</script>

<style scoped>
.container {
  border: 2px soid red;
}
.theme--light.v-card {
  background-color: transparent;
}
.border {
  border: 2px solid red;
}
</style>