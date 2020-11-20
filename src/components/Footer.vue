<template>
  <div class="footer">
    <el-row type="flex" justify="center">
      <el-col :span="6">
        <div class="title">下载qq音乐客户端</div>
        <div class="down">
          <div v-for="i in 4" :key="i" class="item">
            <img src="./windows.png" />
            <div>PC版</div>
          </div>
        </div>
      </el-col>
      <el-col :span="6">
        <div class="title">特色产品</div>
        <div class="down">
          <div v-for="i in 4" :key="i" class="item">
            <img src="./windows.png" />
            <div>PC版</div>
          </div>
        </div>
      </el-col>
      <el-col :span="6">
        <div class="title">合作链接</div>
        <div class="down">
          <div v-for="i in 8" :key="i" class="item">
            QQ
          </div>
        </div>
      </el-col>
    </el-row>
    <el-row type="flex" justify="center">
      <el-col :span="6">
        <div class="title">开放平台</div>
        <div class="down">
          <div v-for="i in 2" :key="i" class="item">
            SDK
          </div>
        </div>
      </el-col>
      <el-col :span="6">
        <div class="title">TME集团官网</div>
        <div class="down">
          腾讯音乐
        </div>
      </el-col>
      <el-col :span="6"></el-col>
    </el-row>
    <el-row type="flex" justify="center" class="about"
      >关于腾讯 | About Tencent | 服务条款 | 用户服务协议 | 隐私政策 | 权利声明 | 广告服务 | 腾讯招聘 | 客服中心 | 网站导航</el-row
    >
    <el-row type="flex" justify="center" class="about"
      >Copyright © 1998 - 2020 Tencent. All Rights Reserved.</el-row
    >
    <el-row type="flex" justify="center" class="about"
      >腾讯公司 版权所有 腾讯网络文化经营许可证</el-row
    >
  </div>
</template>

<script>
import Vue from "vue";
import { Row, Col } from "element-ui";

Vue.component(Row.name, Row);
Vue.component(Col.name, Col);

export default {
  name: "Footer"
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.footer {
  width: 100%;
  background-color: #333;
  color: #999;
  padding: 0 0 20px 0;
}
.down {
  display: flex;
  flex-wrap: wrap;
  img {
    width: 37px;
  }
}
.title {
  margin-top: 80px;
  margin-bottom: 30px;
}
.item {
  margin-right: 50px;
  margin-bottom: 30px;
}
.about {
  font-size: 11px;
  margin-bottom: 10px;
}
</style>
