<template>
  <div class="block">
    <h2>新 歌 首 发</h2>
    <Tabs :tabs="newsongTabs" name="newsongTabs" />
    <el-carousel
      class="carousel"
      height="320px"
      trigger="click"
      indicator-position="outside"
      :autoplay="false"
    >
      <template v-for="k in 5">
        <el-carousel-item :key="k">
          <template v-for="i in 3">
            <el-row
              type="flex"
              :gutter="30"
              justify="center"
              :key="i"
              class="row"
            >
              <template v-for="j in 3">
                <el-col :span="6" :key="j">
                  <SongItem />
                </el-col>
              </template>
            </el-row>
          </template>
        </el-carousel-item>
      </template>
    </el-carousel>
  </div>
</template>

<script>
import Vue from "vue";
import { CarouselItem, Carousel, Row, Col } from "element-ui";
import SongItem from "./SongItem.vue";
import Tabs from "./Tabs.vue";

Vue.component(CarouselItem.name, CarouselItem);
Vue.component(Carousel.name, Carousel);
Vue.component(Row.name, Row);
Vue.component(Col.name, Col);

export default {
  name: "NewSong",
  components: {
    SongItem,
    Tabs
  },
  data: function() {
    return {
      newsongTabs: ["最新", "内地", "港台", "欧美", "韩国", "日本"]
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.block {
  width: 100%;
  padding: 25px 0;
  background: linear-gradient(#f5f5f5, #fff);
  text-align: center;
  h2 {
    font-size: 30px;
  }
}
.row {
  margin: 25px 0;
}
</style>
