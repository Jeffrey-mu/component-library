<template>
  <div class="header">
    <div class="mw h-content">
      <span class="site_name">{{ site_name.split('-')[1] }}</span>
      <div>
        <a href="https://github.com/Jeffrey-mu/">
          <i class="iconfont icon-GitHub"></i>
        </a>
      </div>
    </div>
  </div>
</template>
<script setup>
import { name as site_name } from '../package.json'
import {ref} from 'vue'
console.log(ref);
</script>
<style lang="scss">
.header {
  position: sticky;
  top: 0;
  left: 0;
  box-sizing: border-box;
  padding: 0 20px;
  height: 75px;
  line-height: 75px;
  box-shadow: 1px 2px 10px rgb(226 232 240 / 80%);
  z-index: 99999;
  background: #ffffff;

  .h-content {
    display: flex;
    justify-content: space-between;
    .site_name {
      font-size: 35px;
      font-weight: 700;
    }
  }

}
</style>
