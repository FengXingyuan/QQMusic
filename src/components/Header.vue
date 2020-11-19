<template>
  <div class="header">
    <img
      src="https://y.gtimg.cn/mediastyle/yqq/img/logo.png?nowebp=1"
      class="header__logo"
    />
    <div class="header__left">
      <input type="radio" name="tabs" id="tab1" checked />
      <label class="header__tabs" for="tab1">音乐馆</label>
      <input type="radio" name="tabs" id="tab2" />
      <label class="header__tabs" for="tab2">我的音乐</label>
      <input type="radio" name="tabs" id="tab3" />
      <label class="header__tabs" for="tab3" v-popover:popover>客户端</label>
      <el-popover
        ref="popover"
        content="提示文字"
        title="title"
        trigger="hover"
        width="200"
        visible-arrow="false"
      >
      </el-popover>
      <input type="radio" name="tabs" id="tab4" />
      <label class="header__tabs" for="tab4">开放平台</label>
      <input type="radio" name="tabs" id="tab5" />
      <label class="header__tabs" for="tab5">VIP</label>
    </div>
    <el-dropdown trigger="click" placement="bottom-start">
      <el-input
        class="header__search"
        placeholder="搜索音乐、歌单、MV、用户"
        suffix-icon="el-icon-search"
      >
      </el-input>
      <el-dropdown-menu
        class="dropdown-menu"
        slot="dropdown"
        :visible-arrow="false"
      >
        <MenuItem :id="1" name="我们的歌" :count="89.8" />
        <MenuItem :id="2" name="冰雪奇缘2" :count="76.8" />
        <MenuItem :id="3" name="张杰" :count="54.1" />
        <MenuItem :id="4" name="桥边姑娘" :count="45.9" />
        <MenuItem :id="5" name="星辰大海" :count="34.7" />
        <div class="header__dropdownFooter">
          <div class="header__dropdownFooterTitle">搜索历史</div>
          <i class="el-icon-delete"></i>
        </div>
      </el-dropdown-menu>
    </el-dropdown>
    <div class="header__right">
      <div class="header__login">登录</div>
      <el-dropdown>
        <div class="header__Vip">
          开通VIP<i class="el-icon-arrow-down el-icon--right"></i>
        </div>
        <el-dropdown-menu
          class="dropdown-menu"
          slot="dropdown"
          :visible-arrow="false"
        >
          <div class="header__VipItem">开通绿钻豪华版</div>
          <div class="header__VipDivider"></div>
          <div class="header__VipItem">开通付费包</div>
        </el-dropdown-menu>
      </el-dropdown>
      <el-dropdown>
        <div class="header__Charge">
          充值<i class="el-icon-arrow-down el-icon--right"></i>
        </div>
        <el-dropdown-menu
          class="dropdown-menu"
          slot="dropdown"
          :visible-arrow="false"
        >
          <div class="header__ChargeItem">购买乐币</div>
          <div class="header__ChargeDivider"></div>
          <div class="header__ChargeItem">充值饭票</div>
        </el-dropdown-menu>
      </el-dropdown>
    </div>
  </div>
</template>

<script>
import Vue from "vue";
import { Popover, Dropdown, DropdownMenu, Button, Input } from "element-ui";
import SearchMenuItem from "./SearchMenuItem.vue";

Vue.component(Popover.name, Popover);
Vue.component(Dropdown.name, Dropdown);
Vue.component(DropdownMenu.name, DropdownMenu);
Vue.component(Input.name, Input);
Vue.component(Button.name, Button);
Vue.component("MenuItem", SearchMenuItem);

export default {
  name: "Header"
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  width: 100%;
  height: 90px;
  border-bottom: 1px solid #eee;

  &__logo {
    height: 46px;
    width: 170px;
  }

  &__left {
    display: flex;
  }
  &__tabs {
    display: block;
    height: 90px;
    line-height: 90px;
    padding: 0 20px;
    font-size: 18px;
  }

  &__search {
    width: 220px;
    height: 36px;
  }

  &__dropdownFooter {
    display: flex;
    align-items: center;
    justify-content: space-between;
    margin-top: 10px;
    height: 36px;

    &Title {
      margin-left: 10px;
      color: #bbb;
      font-size: 14px;
    }
    i {
      margin-right: 10px;
    }
  }

  &__right {
    display: flex;
    align-items: center;
  }
  &__login {
    margin-right: 10px;
    font-size: 16px;
    height: 90px;
    line-height: 90px;
    &:hover {
      color: #31c27c;
    }
  }
  &__Vip {
    height: 38px;
    width: 122px;
    font-size: 13px;
    line-height: 38px;
    text-align: center;
    color: white;
    background-color: #31c27c;
    border-radius: 3px;
    &Divider {
      width: 122px;
      border-top: solid 1px #bbb;
    }
    &Item {
      display: flex;
      justify-content: center;
      align-items: center;
      height: 38px;
      width: 122px;
      font-size: 13px;
      &:hover {
        background-color: #31c27c;
        color: white;
      }
    }
  }
  &__Charge {
    margin-left: 10px;
    height: 38px;
    width: 83px;
    font-size: 13px;
    line-height: 38px;
    text-align: center;
    border: 1px solid #bbb;
    border-radius: 3px;
    &Divider {
      width: 83px;
      border-top: solid 1px #bbb;
    }
    &Item {
      display: flex;
      justify-content: center;
      align-items: center;
      height: 38px;
      width: 83px;
      font-size: 13px;
      &:hover {
        background-color: #31c27c;
        color: white;
      }
    }
  }
}

.dropdown-menu {
  padding: 0;
  margin: 0;
}

input[type="radio"] {
  display: none;
}

input[type="radio"]:checked + label {
  background-color: #31c27c;
  color: white;
}

input[type="radio"]:not(:checked) + *:hover {
  color: #31c27c;
}
</style>
