<template>
  <div class="block">
    <h2>歌 单 推 荐</h2>
    <Tabs :tabs="songlistTabs" name="songlistTabs" />
    <el-carousel
      class="carousel"
      height="320px"
      trigger="click"
      indicator-position="outside"
      :autoplay="false"
    >
      <template v-for="j in 3">
        <el-carousel-item :key="j">
          <div class="carousel-inner">
            <AlbumItem descrip="播放量: 1031.7万" v-for="i in 5" :key="i" />
          </div>
        </el-carousel-item>
      </template>
    </el-carousel>
  </div>
</template>

<script>
import Vue from "vue";
import { Carousel, CarouselItem } from "element-ui";
import AlbumItem from "./AlbumItem.vue";
import Tabs from "./Tabs.vue";

Vue.component(Carousel.name, Carousel);
Vue.component(CarouselItem.name, CarouselItem);

export default {
  name: "SongList",
  components: {
    AlbumItem,
    Tabs
  },
  data: function() {
    return {
      songlistTabs: [
        "为您推荐",
        "官方歌单",
        "情歌",
        "网络歌曲",
        "经典",
        "KTV热歌"
      ]
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
.carousel-inner {
  margin: 20px auto;
  width: 75%;
  display: flex;
  justify-content: space-between;
}
</style>
