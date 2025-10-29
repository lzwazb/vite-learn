<script setup>
import HelloWorld from './components/HelloWorld.vue'
import jilian from './components/jilian.vue';
import huakuai from './components/huakuai.vue';
</script>

<template>
  <div>
    <a href="https://vite.dev" target="_blank">
      <img src="/vite.svg" class="logo" alt="Vite logo" />
    </a>
    <a href="https://vuejs.org/" target="_blank">
      <img src="./assets/vue.svg" class="logo vue" alt="Vue logo" />
    </a>
  </div>
  <HelloWorld msg="Vite + Vue" />

  <div class="component-row">
    <jilian></jilian>
    <huakuai></huakuai>
  </div>
  
</template>



<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}

.component-row {
  display: flex;          /* 关键：开启 Flexbox 弹性布局 */
  flex-direction: row;  /* (可选) 默认就是 row (水平) */
  justify-content: center; /* (可选) 让两个组件在水平方向上居中 */
  align-items: flex-start; /* (可选) 顶部对齐 */
  gap: 20px;              /* (可选) 在组件之间添加 20px 的间距 */
  margin-top: 2em;        /* (可选) 离上面的 <HelloWorld> 远一点 */
}
</style>
