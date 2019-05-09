<template>
  <el-menu
    :default-active="activeIndex2"
    class="el-menu-demo"
    mode="horizontal"
    @select="handleSelect"
    background-color="#545c64"
    text-color="#fff"
    active-text-color="#ffd04b"
  >
    <el-menu-item index="1">首页</el-menu-item>
    <el-submenu index="2">
      <template slot="title"
        >电影分类</template
      >
      <el-menu-item index="2-1">动作</el-menu-item>
      <el-menu-item index="2-2">喜剧</el-menu-item>
      <el-menu-item index="2-3">爱情</el-menu-item>
    </el-submenu>
    <el-menu-item index="3" disabled>站长推荐</el-menu-item>
    <el-menu-item index="4">TOP100</el-menu-item>
    <el-menu-item index="5">专题合集</el-menu-item>
    <MovieSearch></MovieSearch>
  </el-menu>
</template>

<script>
import MovieSearch from "./MovieSearch";
export default {
  data() {
    return {
      activeIndex: "1",
      activeIndex2: "1"
    };
  },
  methods: {
    handleSelect(key, keyPath) {
      console.log(key, keyPath);
    }
  },
  components: {
    MovieSearch
  }
};
</script>

<style scoped>
.el-menu-demo {
  display: flex;
  align-items: center;
  justify-content: center;
  margin-bottom: 20px;
}
</style>
