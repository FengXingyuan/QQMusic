<template>
  <div class="block">
    <h2>精 彩 推 荐</h2>
    <el-carousel
      class="carousel"
      height="256px"
      trigger="click"
      indicator-position="outside"
      :autoplay="false"
    >
      <template v-for="j in 3">
        <el-carousel-item :key="j">
          <el-row type="flex" justify="center" gutter="20">
            <el-col :span="9">
              <img
                src="https://y.gtimg.cn/music/common/upload/MUSIC_FOCUS/3246659.jpg?max_age=2592000"
              />
            </el-col>
            <el-col :span="9">
              <img
                src="https://y.gtimg.cn/music/common/upload/MUSIC_FOCUS/3250595.jpg?max_age=2592000"
              />
            </el-col>
          </el-row>
        </el-carousel-item>
      </template>
    </el-carousel>
  </div>
</template>

<script>
import Vue from "vue";
import { Carousel, CarouselItem, Row, Col } from "element-ui";

Vue.component(Carousel.name, Carousel);
Vue.component(CarouselItem.name, CarouselItem);
Vue.component(Row.name, Row);
Vue.component(Col.name, Col);

export default {
  name: "Recommend"
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
  img {
    width: 100%;
  }
}
</style>
