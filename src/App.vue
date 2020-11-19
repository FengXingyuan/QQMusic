<template>
  <div>
    <el-row type="flex" justify="center">
      <el-col :span="18">
        <Header />
      </el-col>
    </el-row>
    <el-row type="flex" justify="center">
      <el-col :span="18">
        <Tabs :tabs="headerTabs" name="headerTabs" />
      </el-col>
    </el-row>
    <SongList />
    <NewSong />
  </div>
</template>

<script>
import Vue from "vue";
import Header from "./components/Header.vue";
import Tabs from "./components/Tabs.vue";
import NewSong from "./components/NewSong.vue";
import SongList from "./components/SongList.vue";
import { Row, Col } from "element-ui";
import "./normalize.css";

Vue.component(Row.name, Row);
Vue.component(Col.name, Col);

export default {
  name: "App",
  components: {
    Header,
    Tabs,
    SongList,
    NewSong
  },
  data: function() {
    return {
      headerTabs: [
        "首页",
        "歌手",
        "新碟",
        "排行榜",
        "分类歌单",
        "电台",
        "MV",
        "数字专辑",
        "票务"
      ]
    };
  }
};
</script>

<style lang="scss">
::v-deep .carousel {
  .el-carousel__arrow {
    height: 100px;
    width: 100px;
  }
}
</style>
