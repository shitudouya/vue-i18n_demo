<template>
  <el-menu
    default-active="1-1"
    background-color="rgb(0, 21, 41)"
    text-color="#fff"
    active-text-color="rgb(45, 140, 240)"
  >
    <el-submenu index="1">
      <template slot="title">
        <i class="el-icon-location"></i>
        <span> {{ $t("aside.home") }}</span>
      </template>
      <el-menu-item-group>
        <el-menu-item index="1-1"> {{ $t("aside.pageOne") }}</el-menu-item>
        <el-menu-item index="1-2">{{ $t("aside.pageTwo") }}</el-menu-item>
      </el-menu-item-group>
    </el-submenu>
    <el-menu-item index="2">
      <i class="el-icon-menu"></i>
      <span slot="title">{{ $t("aside.manage") }}</span>
    </el-menu-item>
    <el-menu-item index="3">
      <i class="el-icon-setting"></i>
      <span slot="title">{{ $t("aside.center") }}</span>
    </el-menu-item>
  </el-menu>
</template>

<script>
export default {};
</script>

<style scoped>
.el-menu {
  height: 100vh;
}
.el-menu >>> .el-submenu-item,
.el-submenu >>> .el-menu-item {
  min-width: 199px;
}
</style>
