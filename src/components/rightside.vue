<template>
    <div class="right">
        <el-col :span="12">
    <el-menu
      default-active="2"
      class="el-menu-vertical-demo"
      @open="handleOpen"
      @close="handleClose"
      background-color="#545c64"
      text-color="#fff"
      style="height:900px;"
      active-text-color="#ffd04b">
      <el-submenu index="1">
        <template slot="title">
          
          <span>Target One</span>
        </template>
        <el-menu-item-group>
          <el-menu-item index="1-1">A</el-menu-item>
          <el-menu-item index="1-2">B</el-menu-item>
        </el-menu-item-group>
        <el-menu-item-group>
          <el-menu-item index="1-3">C</el-menu-item>
        </el-menu-item-group>
        <el-submenu index="1-4">
          <template slot="title">Sub Target One</template>
          <el-menu-item index="1-4-1">P</el-menu-item>
        </el-submenu>
      </el-submenu>
      <el-menu-item index="2">
    
        <span>Target Two</span>
      </el-menu-item>
      <el-menu-item index="3" disabled>
    
        <span>Target Three</span>
      </el-menu-item>
      <el-menu-item index="4">
     
        <span>Target Four</span>
      </el-menu-item>
    </el-menu>
  </el-col>
    </div>
</template>

<script>
  export default {
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