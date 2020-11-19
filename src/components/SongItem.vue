<template>
  <div class="song-item">
    <Album size="song" />
    <div class="middle">
      <div class="song-name">Ready Or Not</div>
      <div class="singer">MOMOLAND</div>
    </div>
    <div class="time">03:20</div>
  </div>
</template>

<script>
import Album from "./Album.vue";
export default {
  name: "SongItem",
  components: {
    Album
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.song-item {
  display: flex;
  align-items: center;
}
.middle {
  display: flex;
  flex-grow: 1;
  margin-left: 20px;
  flex-direction: column;
  justify-content: center;
  align-items: flex-start;
}
.song-name {
  height: 20px;
  font-size: 14px;
  font-weight: 400;
  :hover {
    color: #31c27c;
  }
}
.singer {
  height: 20px;
  font-size: 14px;
  color: #999;
  :hover {
    color: #31c27c;
  }
}
.time {
  flex-grow: none;
  font-size: 14px;
  color: #ddd;
}
</style>
