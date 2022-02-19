<template>
  <v-container>
    <v-row>
      <v-col cols="10">
        <div style="max-width: 60em" class="border py-5">
          <v-row align="center" no-gutters>
            <v-col cols="3" class="pl-10">学校ｺｰﾄﾞ</v-col>
            <v-col cols="7">
              <v-text-field></v-text-field>
            </v-col>
          </v-row>
          <v-row align="center" no-gutters>
            <v-col cols="3" class="pl-10">校種</v-col>
            <v-col cols="7">
              <v-select :items="sampleItems"></v-select>
            </v-col>
          </v-row>
          <v-row align="center" no-gutters>
            <v-col cols="3" class="pl-10">地区コード</v-col>
            <v-col cols="7">
              <v-select :items="sampleItems"></v-select>
            </v-col>
          </v-row>
          <v-row align="center" no-gutters>
            <v-col cols="3" class="pl-10">学区ｺｰﾄﾞ</v-col>
            <v-col cols="7">
              <v-select :items="sampleItems"></v-select>
            </v-col>
          </v-row>
          <v-row align="center" no-gutters>
            <v-col cols="3" class="pl-10">学校立ｺｰﾄﾞ</v-col>
            <v-col cols="7">
              <v-select :items="sampleItems"></v-select>
            </v-col>
          </v-row>
          <v-row align="center" no-gutters>
            <v-col cols="3" class="pl-10">学校名</v-col>
            <v-col cols="7">
              <v-text-field></v-text-field>
            </v-col>
          </v-row>
          <v-row align="center" no-gutters>
            <v-col cols="3" class="pl-10">学校名かな</v-col>
            <v-col cols="7">
              <v-text-field></v-text-field>
            </v-col>
          </v-row>
          <v-row align="center" no-gutters>
            <v-col cols="3" class="pl-10">学校名略称</v-col>
            <v-col cols="7">
              <v-text-field></v-text-field>
            </v-col>
          </v-row>
          <v-row align="center" no-gutters>
            <v-col cols="3" class="pl-10">学校名略称かな</v-col>
            <v-col cols="7">
              <v-text-field></v-text-field>
            </v-col>
          </v-row>
          <v-row align="center" no-gutters>
            <v-col cols="3" class="pl-10">学校長氏名</v-col>
            <v-col cols="7">
              <v-text-field></v-text-field>
            </v-col>
          </v-row>
          <v-row align="center" no-gutters>
            <v-col cols="3" class="pl-10">学校長氏名かな</v-col>
            <v-col cols="7">
              <v-text-field></v-text-field>
            </v-col>
          </v-row>
          <v-row align="center" no-gutters>
            <v-col cols="3" class="pl-10">担当者</v-col>
            <v-col cols="7">
              <v-select :items="sampleItems"></v-select>
            </v-col>
          </v-row>
          <v-row align="center" no-gutters>
            <v-col cols="3" class="pl-10">都道府県</v-col>
            <v-col cols="7">
              <v-select :items="sampleItems"></v-select>
            </v-col>
          </v-row>
          <v-row align="center" no-gutters>
            <v-col cols="3" class="pl-10">市町村</v-col>
            <v-col cols="7">
              <v-select :items="sampleItems"></v-select>
            </v-col>
          </v-row>
          <v-row align="center" no-gutters>
            <v-col cols="3" class="pl-10">郵便番号</v-col>
            <v-col cols="7">
              <v-text-field></v-text-field>
            </v-col>
          </v-row>
          <v-row align="center" no-gutters>
            <v-col cols="3" class="pl-10">住所</v-col>
            <v-col cols="7">
              <v-text-field></v-text-field>
            </v-col>
          </v-row>
          <v-row align="center" no-gutters>
            <v-col cols="3" class="pl-10">方書き</v-col>
            <v-col cols="7">
              <v-text-field></v-text-field>
            </v-col>
          </v-row>
          <v-row align="center" no-gutters>
            <v-col cols="3" class="pl-10">電話番号</v-col>
            <v-col cols="7">
              <v-text-field></v-text-field>
            </v-col>
          </v-row>
          <v-row align="center" no-gutters>
            <v-col cols="3" class="pl-10">FAX番号</v-col>
            <v-col cols="7">
              <v-text-field></v-text-field>
            </v-col>
          </v-row>
          <v-row align="center" no-gutters>
            <v-col cols="3" class="pl-10">教育委員会ｺｰﾄﾞ</v-col>
            <v-col cols="7">
              <v-select :items="sampleItems"></v-select>
            </v-col>
          </v-row>
          <v-row align="center" no-gutters>
            <v-col cols="3" class="pl-10">統廃合</v-col>
            <v-col cols="7">
              <v-checkbox dense hide-details></v-checkbox>
            </v-col>
          </v-row>
          <v-row align="center" no-gutters>
            <v-col cols="3" class="pl-10">指導要録用「卒業」</v-col>
            <v-col cols="7">
              <v-checkbox label="印字しない" dense hide-details></v-checkbox>
            </v-col>
          </v-row>
          <v-row class="text-right">
            <v-col class="col-10">
              <v-btn color="primary" depressed rounded class="mr-3">登録</v-btn>
              <v-btn depressed rounded class="mr-3">キャンセル</v-btn>
            </v-col>
          </v-row>
        </div>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "Register",
  data() {
    return {
      sampleItems: ["項目その1", "項目その2", "項目その3", "項目その4"],
    };
  },
};
</script>

<style scoped>
.border {
  border: 2px solid red;
}
</style>