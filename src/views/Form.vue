<script lang="ts" setup>
import { reactive } from 'vue'
import Editor from '@tinymce/tinymce-vue'

const form = reactive({
  name: '',
  region: '',
  date1: '',
  date2: '',
  delivery: false,
  type: [],
  resource: '',
  desc: '',
})
</script>

<template>
  <el-form :model="form" label-width="120px">
    <el-form-item label="标题">
      <el-input v-model="form.name" />
    </el-form-item>
    <el-form-item label="义项名">
      <el-input v-model="form.name" />
    </el-form-item>
    <el-form-item label="概述">
      <el-input v-model="form.name" />
    </el-form-item>
    <el-form-item label="图片">
      <el-input v-model="form.name" />
    </el-form-item>
    <el-form-item label="分类">
      <el-select v-model="form.region" placeholder="please select your zone">
        <el-option label="Zone one" value="shanghai" />
        <el-option label="Zone two" value="beijing" />
      </el-select>
    </el-form-item>
    <el-form-item label="正文">
      <editor api-key='fjh619ssikex92wq76ifinvsw9ow4tugkio35ngfbhof7mz5' :init="{
        plugins: 'lists link image table code help wordcount'
      }" />
    </el-form-item>
    <el-form-item label="参考资料">
      <el-input v-model="form.name" />
    </el-form-item>
  </el-form>
</template>