<template>
  <div :class="'album-' + size">
    <div :class="'play-' + size">
      <img src="./play.png" />
    </div>
  </div>
</template>

<script>
export default {
  name: "Album",
  props: {
    size: String
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.album-big {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 224px;
  width: 224px;
  transition: all 0.5s ease;
  background-position: center;
  background-size: 100%;
  background-image: url("https://qpic.y.qq.com/music_cover/JMO8g4MPROhBr59X2g0aibqiakHE0S12OOhUf7iav9yuThf1xMnm4ibemA/300?n=1");
  &:hover {
    background-size: 110%;
    .play-big {
      opacity: 1;
      height: 60px;
      width: 60px;
      border-radius: 30px;
    }
    img {
      width: 30px;
      height: 30px;
    }
  }
}
.album-song {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 86px;
  width: 86px;
  transition: all 0.5s ease;
  background-position: center;
  background-size: 100%;
  background-image: url("https://qpic.y.qq.com/music_cover/JMO8g4MPROhBr59X2g0aibqiakHE0S12OOhUf7iav9yuThf1xMnm4ibemA/300?n=1");
  &:hover {
    background-size: 110%;
    .play-song {
      opacity: 1;
      height: 40px;
      width: 40px;
      border-radius: 20px;
    }
    img {
      width: 20px;
      height: 20px;
    }
  }
}
.album-mv {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 126px;
  width: 224px;
  transition: all 0.5s ease;
  background-position: center;
  background-size: 100%;
  background-image: url("https://qpic.y.qq.com/music_cover/JMO8g4MPROhBr59X2g0aibqiakHE0S12OOhUf7iav9yuThf1xMnm4ibemA/300?n=1");
  &:hover {
    background-size: 110%;
    .play-mv {
      opacity: 1;
      height: 60px;
      width: 60px;
      border-radius: 30px;
    }
    img {
      width: 30px;
      height: 30px;
    }
  }
}
.play-big {
  display: flex;
  align-items: center;
  justify-content: center;
  opacity: 0;
  height: 50px;
  width: 50px;
  border-radius: 25px;
  background-color: white;
  transition: all 0.5s ease;
  img {
    transition: all 0.5s ease;
    width: 25px;
    height: 25px;
  }
}
.play-mv {
  display: flex;
  align-items: center;
  justify-content: center;
  opacity: 0;
  height: 50px;
  width: 50px;
  border-radius: 25px;
  background-color: white;
  transition: all 0.5s ease;
  img {
    transition: all 0.5s ease;
    width: 25px;
    height: 25px;
  }
}
.play-song {
  display: flex;
  align-items: center;
  justify-content: center;
  opacity: 0;
  height: 40px;
  width: 40px;
  border-radius: 20px;
  background-color: white;
  transition: all 0.5s ease;
  img {
    transition: all 0.5s ease;
    width: 20px;
    height: 20px;
  }
}
</style>
