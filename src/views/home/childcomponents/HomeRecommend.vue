<template>
  <div class="home-recommend">
    <div class="item" v-for="(item, index) in recommends" :key="index">
      <a :href="item.link">
        <img :src="item.image" />
        <div>{{ item.title }}</div>
      </a>
    </div>
  </div>
</template>

<script>
export default {
  name: "HomeRecommend",
  props: {
    recommends: {
      type: Array,
      defalut() {
        return [];
      },
    },
  },
};
</script>

<style>
.home-recommend {
  display: flex;
  width: 100%;
  font-size: 14px;
  border-bottom: 10px solid #eee;
}
.home-recommend .item {
  flex: 1;
  text-align: center;
  margin: 6px 0 10px;
}
.home-recommend img {
  width: 70px;
  margin-bottom: 6px;
}
</style>