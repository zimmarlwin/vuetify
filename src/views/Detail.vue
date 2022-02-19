<template>
  <v-container>
    <v-row>
      <v-col cols="10">
        <div style="max-width: 60em" class="border py-5">
          <v-row class="text-right">
            <v-col class="col-10">
              <v-btn color="primary" depressed rounded class="mr-3">
                <v-icon left>edit</v-icon>
                <span>編集</span>
              </v-btn>
              <v-btn color="red white--text" depressed rounded class="mr-3">
                <v-icon left>delete</v-icon>
                <span>削除</span>
              </v-btn>
            </v-col>
          </v-row>
          <v-row>
            <v-col cols="10">
              <v-simple-table>
                <template v-slot:default>
                  <tbody>
                    <tr>
                      <td>出欠ｺｰﾄﾞ</td>
                      <td>0</td>
                    </tr>
                    <tr>
                      <td>出欠名称</td>
                      <td>出席</td>
                    </tr>
                    <tr>
                      <td>処理読替</td>
                      <td></td>
                    </tr>
                    <tr>
                      <td>出欠記号</td>
                      <td>出</td>
                    </tr>
                    <tr>
                      <td>カウント倍数</td>
                      <td></td>
                    </tr>
                    <tr>
                      <td>管理者以外表示可</td>
                      <td></td>
                    </tr>
                    <tr>
                      <td>全校時の出欠ｺｰﾄﾞ</td>
                      <td>出席</td>
                    </tr>
                    <tr>
                      <td>出欠入力表示順</td>
                      <td>1</td>
                    </tr>
                    <tr>
                      <td>出欠届け表示順</td>
                      <td>1</td>
                    </tr>
                    <tr>
                      <td>読替先処理ｺｰﾄﾞ</td>
                      <td>出席</td>
                    </tr>
                  </tbody>
                </template>
              </v-simple-table></v-col
            >
          </v-row>
        </div>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "Detail",
};
</script>

<style scoped>
.border {
  border: 2px solid red;
}
</style>