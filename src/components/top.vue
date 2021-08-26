<template>

<div class="menu">
<el-menu
:default-active="activeIndex2"
  class="el-menu-demo"
  mode="horizontal"
  @select="handleSelect"
  background-color="#545c64"
  text-color="#fff"
  active-text-color="#ffd04b">
  <el-menu-item index="1" style="font-size:20px;">Bikers</el-menu-item>
  <el-submenu index="2" style="margin-left:400px;">
    <template slot="title" >Service Station</template>
    <el-menu-item index="2-1">Delhi</el-menu-item>
    <el-menu-item index="2-2">Pune</el-menu-item>
    <el-menu-item index="2-3">Banglore</el-menu-item>
    <el-submenu index="2-4">
      <template slot="title">Mumbai</template>
      <el-menu-item index="2-4-1">Kalyan</el-menu-item>
      <el-menu-item index="2-4-2">Thane</el-menu-item>
      <el-menu-item index="2-4-3">Navi Mumbai</el-menu-item>
    </el-submenu>
  </el-submenu>
  <el-menu-item index="3" disabled style="margin-left:200px;"> Delivery</el-menu-item>
  <el-menu-item index="4" style="margin-left:200px;"><a href="https://www.royalenfield.com/" target="_blank">Royal Enfield</a></el-menu-item>
</el-menu>
</div>
</template>

<style>
.menu{
    margin-top:0px;
}
</style>

<script>
  export default {
    data() {
      return {
        activeIndex: '1',
        activeIndex2: '1'
      };
    },
    methods: {
      handleSelect(key, keyPath) {
        console.log(key, keyPath);
      }
    }
  }
</script>