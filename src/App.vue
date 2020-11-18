<template>
  <el-row type="flex" justify="center">
    <el-col :span="18">
      <Header />
    </el-col>
  </el-row>
</template>

<script>
import Vue from "vue";
import Header from "./components/Header.vue";
import { Row, Col } from "element-ui";
import "./normalize.css";

Vue.component(Row.name, Row);
Vue.component(Col.name, Col);

export default {
  name: "App",
  components: {
    Header
  }
};
</script>

<style lang="scss"></style>
