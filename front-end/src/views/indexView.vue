<script setup>
  import {logout} from "@/net";
  import router from "@/router";

  function userLogout() {
    logout(() => {
      router.push('/')
    });
  }
</script>

<template>
  <div class="exit">
    <el-button @click="userLogout" type="danger">退出登录</el-button>
  </div>
</template>

<style scoped>
.exit{
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
</style>