<template>
  <div class="tabs">
    <input type="radio" :name="name" :id="name" checked />
    <label class="tabs__item" :for="name">{{ tabs[0] }}</label>
    <template v-for="(item, index) in list">
      <input type="radio" :name="name" :id="name + index" :key="name + index" />
      <label class="tabs__item" :for="name + index" :key="name + index">
        {{ item }}
      </label>
    </template>
  </div>
</template>

<script>
export default {
  name: "",
  props: {
    tabs: Array,
    name: String
  },
  computed: {
    list: function() {
      return this.tabs.slice(1);
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.tabs {
  width: 100%;
  height: 51px;
  line-height: 51px;
  display: flex;
  justify-content: center;
  input[type="radio"] {
    display: none;
  }
  &__item {
    margin: 0 24px;
    font-size: 15px;
    &:hover {
      color: #31c27c;
    }
  }
}

input[type="radio"]:checked + label {
  color: #31c27c;
}
</style>
