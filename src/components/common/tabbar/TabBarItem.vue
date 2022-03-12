<template>
  <!-- 注意：将插槽都用一层div包裹，这样属性便可写在div上，防止插槽被替换时属性也没有了 -->
  <div class="tab-bar-item" @click="itemClick">
    <div v-if="!isActive">
      <slot name="item-img"></slot>
    </div>
    <div v-else>
      <slot name="item-img-active"></slot>
    </div>
    <!-- 动态绑定样式，复杂时抽取为计算属性 -->
    <div :style="finalStyle">
      <slot name="item-text"></slot>
    </div>
  </div>
</template>

<script>
export default {
  name: "TabBarItem",
  props: {
    // 路由路径
    path: String,
    // 文字颜色
    activeColor: {
      type: String,
      default: "#ff5777",
    },
  },
  data() {
    return {};
  },
  computed: {
    // 是否被点击
    isActive() {
      // 判断条件：当前的导航路径是否包含选择的子组件传过来的path
      return this.$route.path.indexOf(this.path) !== -1;
    },
    // 文字颜色
    finalStyle() {
      return this.isActive ? { color: this.activeColor } : {};
    },
  },
  methods: {
    itemClick() {
      // 路由跳转
      this.$router.push(this.path);
    },
  },
};
</script>

<style>
.tab-bar-item {
  flex: 1;
  text-align: center;
  height: 49px;
  font-size: 14px;
}
.tab-bar-item img {
  height: 24px;
  margin-top: 3px;
  vertical-align: middle;
}
</style>