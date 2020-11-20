<template>
  <div class="album-item">
    <Album size="mv" />
    <p class="title">Radio</p>
    <p class="descrip">刘宪华</p>
  </div>
</template>

<script>
import Album from "./Album.vue";

export default {
  name: "MVItemItem",
  components: {
    Album
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
