<script setup>
import { ref } from 'vue'

// 来自第一个 script
defineProps({
  msg: String,
})
const count = ref(0)

// 来自第二个 script
const radio = ref(3) // 确保 ref 只从 'vue' 导入一次
</script>

<template>
  <h1>{{ msg }}</h1>

  <div class="card">
    <button type="button" @click="count++">count is {{ count }}</button>
    <p>
      Edit
      <code>components/HelloWorld.vue</code> to test HMR
    </p>
  </div>

  <p>
    Check out
    <a href="https://vuejs.org/guide/quick-start.html#local" target="_blank"
      >create-vue</a
    >, the official Vue + Vite starter
  </p>
  <p>
    Learn more about IDE Support for Vue in the
    <a
      href="https://vuejs.org/guide/scaling-up/tooling.html#ide-support"
      target="_blank"
      >Vue Docs Scaling up Guide</a
    >.
  </p>
  <p class="read-the-docs">Click on the Vite and Vue logos to learn more</p>

  <el-radio-group v-model="radio" style="margin-top: 20px;">
    <el-radio :label="3">Option A</el-radio>
    <el-radio :label="6">Option B</el-radio>
    <el-radio :label="9">Option C</el-radio>
  </el-radio-group>
  <p>你选择的是: {{ radio }}</p>

</template>

<style scoped>
.read-the-docs {
  color: #888;
}
</style>