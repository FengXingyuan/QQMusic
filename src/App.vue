<template>
  <div class="outer">
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
    <Recommend />
    <NewDisc />
    <Ranking />
    <MV />
    <Footer />
    <div class="backtop"><i class="el-icon-arrow-up"></i></div>
    <div class="feedback">反馈</div>
    <div class="play"><i class="el-icon-video-play"></i></div>
    <div class="download"><img src="./7.png" /></div>
  </div>
</template>

<script>
import Vue from "vue";
import Header from "./components/Header.vue";
import Tabs from "./components/Tabs.vue";
import NewSong from "./components/NewSong.vue";
import SongList from "./components/SongList.vue";
import NewDisc from "./components/NewDisc.vue";
import Recommend from "./components/Recommend.vue";
import Ranking from "./components/Ranking.vue";
import MV from "./components/MV.vue";
import Footer from "./components/Footer.vue";
import { Row, Col } from "element-ui";
import "./normalize.css";
import "./global.css";

Vue.component(Row.name, Row);
Vue.component(Col.name, Col);

export default {
  name: "App",
  components: {
    Header,
    Tabs,
    SongList,
    NewSong,
    NewDisc,
    Recommend,
    Ranking,
    MV,
    Footer
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
.backtop {
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 25px;
  position: fixed;
  bottom: 124px;
  right: 40px;
  height: 38px;
  width: 38px;
  border: 1px solid #c9c9c9;
  background-color: white;
  z-index: 5;
}
.feedback {
  display: flex;
  align-items: center;
  justify-content: center;
  position: fixed;
  bottom: 82px;
  right: 40px;
  height: 38px;
  width: 38px;
  border: 1px solid #c9c9c9;
  background-color: white;
  font-size: 14px;
  z-index: 5;
}
.play {
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 25px;
  position: fixed;
  bottom: 40px;
  right: 40px;
  height: 38px;
  width: 38px;
  border: 1px solid #c9c9c9;
  background-color: white;
  z-index: 5;
}
.download {
  position: fixed;
  top: 164px;
  right: 40px;
  height: 132px;
  width: 180px;
  z-index: 5;
  img {
    width: 180px;
    border-radius: 3px;
  }
}
</style>
