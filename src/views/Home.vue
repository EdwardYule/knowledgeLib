<script setup lang="ts">
import { ref } from 'vue'
const list = ref([
  {
    name: "小明",
    idCard: "132456",
  }
]);
const getList = () => {
  console.log('ddd');
}
</script>

<template>
  <h1 class="title">身份证生成工具</h1>
  <div class="operations">
    <el-button @click="getList" type="primary">生成</el-button>
  </div>
  <el-table :data="list">
    <el-table-column prop="name" label="姓名"></el-table-column>
    <el-table-column prop="idCard" label="身份证"></el-table-column>
  </el-table>
</template>

<style scoped lang="scss">
.title{
  text-align: center;
}
.operations{
  display: flex;
  justify-content: center;
}
</style>