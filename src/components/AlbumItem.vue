<template>
  <div class="album-item">
    <Album size="big" />
    <p class="title">王者荣耀</p>
    <p class="descrip">{{ descrip }}</p>
  </div>
</template>

<script>
import Album from "./Album.vue";

export default {
  name: "AlbumItem",
  components: {
    Album
  },
  props: {
    descrip: String
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.album-item {
  width: 224px;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
}
.title {
  font-size: 16px;
  line-height: 1.5;
  margin: 15px 0 0 0;
}
.descrip {
  margin: 0;
  font-size: 14px;
  color: #999;
}
</style>
