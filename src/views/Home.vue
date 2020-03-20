<template>
  <el-container>
    <el-aside width="200px">
      <Aside/>
    </el-aside>
    <el-container>
      <el-header>
        <CommonHeader/>
      </el-header>
      <el-main></el-main>
    </el-container>
  </el-container>
</template>

<script>
import Aside from "../components/Aside";
import CommonHeader from '../components/CommonHeader';
export default {
  name: "Home",
  components: {
    Aside,
    CommonHeader
  }
};
</script>

<style scoped>
.el-header {
    padding: 0px;
}
.el-main {
  background-color: #f5f5f5;
}
</style>
