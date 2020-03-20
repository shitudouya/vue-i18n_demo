<template>
  <header>
    <span> {{ $t("header.home") }}</span>
    <el-dropdown @command="handleCommand">
      <span class="el-dropdown-link">
        {{ $t("header.lang") }}<i class="el-icon-arrow-down el-icon--right"></i>
      </span>
      <el-dropdown-menu slot="dropdown">
        <el-dropdown-item command="zh">中文</el-dropdown-item>
        <el-dropdown-item command="en">English</el-dropdown-item>
      </el-dropdown-menu>
    </el-dropdown>
  </header>
</template>

<script>
import Cookies from "js-cookie";
export default {
  data() {
    return {};
  },
  methods: {
    handleCommand(command) {
      this.$i18n.locale = command;
      Cookies.set("language", command);
    }
  }
};
</script>

<style scoped>
header {
  height: 100%;
  display: flex;
  padding: 0 20px;
  align-items: center;
  justify-content: space-between;
  box-shadow: 0 1px 4px rgba(0, 21, 41, 0.08);
  background-color: #fff;
}
.el-dropdown {
  float: right;
}
.el-dropdown-link {
  cursor: pointer;
  color: #409eff;
}
.el-icon-arrow-down {
  font-size: 12px;
}
</style>
