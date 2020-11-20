<template>
  <div class="block">
    <h2>排 行 榜</h2>
    <div class="inner">
      <img src="./1.png" />
      <img src="./2.png" />
      <img src="./3.png" />
      <img src="./4.png" />
      <img src="./5.png" />
    </div>
  </div>
</template>

<script>
export default {
  name: "Ranking"
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
    width: 224px;
  }
}
.inner {
  display: flex;
  justify-content: space-between;
  margin: 0 auto;
  width: 75%;
}
</style>
