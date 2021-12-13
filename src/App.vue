<template>
  <div id="app">
    <el-container>
      <el-header class="header"><page-header></page-header></el-header>
      <el-main class="main"><router-view /></el-main>
    </el-container>
  </div>
</template>
<script>
import Header from '@/components/Header.vue';
export default {
  components: {
    'page-header': Header,
  },
};
</script>

<style lang="less">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale; 
  color: #2c3e50;
}
.header {
  padding: 0;
}
.main{
  margin: 0 auto;
  width: 1200px;
  padding: 20px 0;
}
</style>
