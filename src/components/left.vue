<template>
    
        <el-menu
          :default-active="activeIndex"
          background-color="#333"
          text-color="#fff"
          active-text-color="yellow"
          class="el-menu-vertical-demo"
          :collapse="false"
          router
        >
        <el-menu-item index="1" route="/">
            <i class="el-icon-setting"></i>
            <span slot="title">工作平台</span>
          </el-menu-item>
          <el-submenu index="2">
            <template slot="title">
              <i class="el-icon-location"></i>
              <span slot="title">用户管理</span>
            </template>
            <el-menu-item-group>
              <el-menu-item index="2-1" route="/user">用户列表</el-menu-item>
              <el-menu-item index="2-2">选项2</el-menu-item>
            </el-menu-item-group>
            <el-menu-item-group >
              <el-menu-item index="2-3">选项3</el-menu-item>
            </el-menu-item-group>
          </el-submenu>
          <el-menu-item index="3">
            <i class="el-icon-menu"></i>
            <span slot="title">导航二</span>
          </el-menu-item>
          
          
        </el-menu>
    
</template>

<script>
export default {
  data(){
    return{
      activeIndex:"1"
    }
  }
}
</script>