<template>
  <tab-bar>
    <tab-bar-item path="/home">
      <img slot="item-img" src="~assets/img/tabbar/home.svg" alt="首页" />
      <img
        slot="item-img-active"
        src="~assets/img/tabbar/home_active.svg"
        alt="首页"
      />
      <div slot="item-text">首页</div>
    </tab-bar-item>
    <tab-bar-item path="/category">
      <img slot="item-img" src="~assets/img/tabbar/category.svg" alt="分类" />
      <img
        slot="item-img-active"
        src="~assets/img/tabbar/category_active.svg"
        alt="首页"
      />
      <div slot="item-text">分类</div>
    </tab-bar-item>
    <tab-bar-item path="/cart">
      <img slot="item-img" src="~assets/img/tabbar/shopcart.svg" alt="购物车" />
      <img
        slot="item-img-active"
        src="~assets/img/tabbar/shopcart_active.svg"
        alt="首页"
      />
      <div slot="item-text">购物车</div>
    </tab-bar-item>
    <tab-bar-item path="/profile">
      <img slot="item-img" src="~assets/img/tabbar/profile.svg" alt="我的" />
      <img
        slot="item-img-active"
        src="~assets/img/tabbar/profile_active.svg"
        alt="首页"
      />
      <div slot="item-text">我的</div>
    </tab-bar-item>
  </tab-bar>
</template>

<script>
import TabBar from "components/common/tabbar/TabBar.vue";
import TabBarItem from "components/common//tabbar/TabBarItem.vue";

export default {
  name: "MainTabBar",
  components: {
    TabBar,
    TabBarItem,
  },
};
</script>

<style>
</style>