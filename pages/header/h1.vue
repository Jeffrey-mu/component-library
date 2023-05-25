
<template>
  <div>
    <div class="f_header"> <i class="iconfont icon-shouye"></i> <span>{{ site_name }}</span><i
        class="iconfont icon-caidanshezhi"></i>
    </div>
  </div>
</template>
<script setup>
import { name as site_name } from '../../package.json'

</script>
<style lang="scss">
.f_header {
  height: 50px;
  width: 100%;
  display: flex;
  justify-content: space-between;
  border-bottom: 2px solid black;
  line-height: 50px;
  box-sizing: border-box;

  @media screen and (max-width: 750px) {
    padding: 0 20px;
  }
}
</style>
