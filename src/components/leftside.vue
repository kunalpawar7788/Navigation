<template>
    
<div id="app">
<el-radio-group v-model="isCollapse">
  <el-radio-button :label="true">X</el-radio-button>
  <el-radio-button :label="false">O</el-radio-button>
</el-radio-group>
<el-menu style="height: 900px; margin-top:-50px;" background-color="#545c64" text-color="#fff" default-active="2" class="el-menu-vertical-demo" @open="handleOpen" @close="handleClose" :collapse="isCollapse">
  <el-submenu index="1" >
    <template slot="title">
      <i class="el-icon-location" style="color:white;"></i>
      <span slot="title" style="padding-left:-20px; font-size:18px; font-style:bold;">Home</span>
    </template>
    <el-menu-item-group>
      <span slot="title" style="font-size:16px; color:orange;">Safety kit</span>
      <el-menu-item index="1-1" style="padding-right:30px; font-size:14px;">Helmet</el-menu-item>
      <el-menu-item index="1-2" style="padding-right:30px; font-size:14px;">Jacket</el-menu-item>
    </el-menu-item-group>
    <el-menu-item-group >
      <span slot="title" style="font-size:16px; color:orange;">Accessory</span>
      <el-menu-item index="1-3" style="padding-right:30px; font-size:14px;">Gloves</el-menu-item>
    </el-menu-item-group>
    <el-submenu index="1-4">
      <span slot="title" style="font-size:16px; color:lightgreen; margin-left:-10px;">Models</span>
      <el-menu-item index="1-4-1">Thunderbird</el-menu-item>
      <el-submenu index="1-5">
          <span slot="title" style="color:lightblue;">Classic 350</span>
          <el-menu-item index="1-5-1">Standard</el-menu-item>
      </el-submenu>
      <el-menu-item index="1-4-2">Interceptor</el-menu-item>
      <el-menu-item index="1-4-3">Continental</el-menu-item>
    </el-submenu>
  </el-submenu>
  <el-menu-item index="2">
    <i class="el-icon-menu"></i>
    <span slot="title">Contact Us</span>
  </el-menu-item>
  <el-menu-item index="3" disabled>
    <i class="el-icon-document" style="color:white;"></i>
    <span slot="title">About Us</span>
  </el-menu-item>
  <el-menu-item index="4">
    <i class="el-icon-setting" style="color:white;"></i>
    <span slot="title">FAQ</span>
  </el-menu-item>
</el-menu>
</div>
</template>

<style>
  .el-menu-vertical-demo:not(.el-menu--collapse) {
    width: 200px;
    min-height: 400px;
  }
</style>
<script>
  export default {
    data() {
      return {
        isCollapse: true
      };
    },
    methods: {
      handleOpen(key, keyPath) {
        console.log(key, keyPath);
      },
      handleClose(key, keyPath) {
        console.log(key, keyPath);
      }
    }
  }
</script>