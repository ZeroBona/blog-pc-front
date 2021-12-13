<template>
  <div class="header">
    <div class="logo"><img src="../assets/images/blog-logo.png" alt="无法加载"></div>
    <el-menu
      :default-active="activeIndex"
      :router="true"
      mode="horizontal"
      background-color="#347fff"
      text-color="#ffffff"
      active-text-color="#ffffff"
    >
      <el-menu-item index="/">首页</el-menu-item>
      <el-menu-item index="/profile">个人</el-menu-item>
    </el-menu>
  </div>
</template>

<script>
export default {
  components: {},
  props: {},
  data() {
    return {
      activeIndex: '/',
    };
  },
  computed: {},
  methods: {},
  created() {},
  mounted() {},
};
</script>
<style lang="less" scoped>
.header{
  display: flex;
  align-items: center;
  background-color: #347fff;
  height: 60px;
}
.logo{
  display: flex;
  justify-content: center;
  align-items: center;
  width: 200px;
  height: 60px;
  img{
    height: 80%;
  }
}
</style>
