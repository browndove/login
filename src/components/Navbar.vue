<template >
    <div class="navbar">
        <section >
            <img src="/images/logo.png" alt="" style="width: 200px;">
        </section>

        <section>
            <el-menu
    default-active="1"
    class="el-menu-demo"
    mode="horizontal"
    @select="handleSelect"
    :ellipsis="false"
  >
  <el-menu-item index="1">Home</el-menu-item>
  <el-sub-menu index="2">
    <template #title>Courses</template>
    <el-menu-item index="2-1">item one</el-menu-item>
    <el-menu-item index="2-2">item two</el-menu-item>
    <el-menu-item index="2-3">item three</el-menu-item>
  </el-sub-menu>
  <!-- questions -->
  <el-sub-menu index="2">
    <template #title>Questions</template>
    <el-menu-item index="2-1">item one</el-menu-item>
    <el-menu-item index="2-2">item two</el-menu-item>
    <el-menu-item index="2-3">item three</el-menu-item>
  </el-sub-menu>
  <!-- products -->
  <el-sub-menu index="3">
    <template #title>Product</template>
    <el-menu-item index="3-1">item one</el-menu-item>
    <el-menu-item index="3-2">item two</el-menu-item>
    <el-menu-item index="3-3">item three</el-menu-item>
  </el-sub-menu>
  <!-- Pricing -->
  <el-menu-item index="4">Pricing</el-menu-item>
</el-menu>
        </section>


        <section class="log_sign">
            <el-button>Default</el-button>
            <el-button type="success">Success</el-button>
        </section>
    </div>
</template>


<script>
export default {
    name: "NavbarComponent"
}
</script>

<script setup>
import {ref} from "vue"

function handleSelect(val, event) {
    console.log(val)
    
}
</script>

<style >
    .navbar{
        display: flex;
        justify-content: space-between;
        align-items: center;
    }
    .el-menu--horizontal{
        align-items: center;
    }
    .el-menu--horizontal.el-menu {
        border-bottom: none !important;
    }
    .log_sign{
        display: flex;
        justify-content: center;
        align-items: center;
    }
    img{
        margin-top: 10px;
    }
</style>