<template>
  <div class="item">
    <div class="item__id">{{ id }}</div>
    <div class="item__name">{{ name }}</div>
    <div class="item__count">{{ count + "万" }}</div>
  </div>
</template>

<script>
export default {
  name: "",
  props: {
    id: Number,
    name: String,
    count: Number
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.item {
  display: flex;
  align-items: center;
  width: 220px;
  height: 30px;

  &__id {
    flex: none;
    margin-left: 10px;
    color: red;
    font-size: 14px;
  }
  &__name {
    flex: 1;
    margin-left: 10px;
    font-size: 14px;
  }
  &__count {
    flex: none;
    margin-right: 10px;
    font-size: 11px;
    color: #bbb;
  }

  &:hover {
    background-color: #31c27c;
    div {
      color: white;
    }
  }
}
</style>
