<template>
  <div class="block">
    <h2>MV</h2>
    <Tabs :tabs="newdiscTabs" name="newdiscTabs" />
    <el-carousel
      class="carousel"
      height="420px"
      trigger="click"
      indicator-position="outside"
      :autoplay="false"
    >
      <template v-for="j in 3">
        <el-carousel-item :key="j">
          <div class="carousel-inner">
            <MVItem v-for="i in 5" :key="i" />
          </div>
          <div class="carousel-inner">
            <MVItem v-for="i in 5" :key="i" />
          </div>
        </el-carousel-item>
      </template>
    </el-carousel>
  </div>
</template>

<script>
import Vue from "vue";
import { Carousel, CarouselItem } from "element-ui";
import MVItem from "./MVItem.vue";
import Tabs from "./Tabs.vue";

Vue.component(Carousel.name, Carousel);
Vue.component(CarouselItem.name, CarouselItem);

export default {
  name: "NewDisc",
  components: {
    MVItem,
    Tabs
  },
  data: function() {
    return {
      newdiscTabs: ["精选", "内地", "港台", "欧美", "韩国", "日本", "其他"]
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
