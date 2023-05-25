<template>
  <div class="tools">
    <select name="" id="" v-model="size">
      <option :value="item"  v-for="item in Object.keys(sizes)">{{ item }}</option>
    </select>
  </div>
  <Hako h="full" w="full" :width="width" :height="height" class="window">
    <!-- <Preview shadow="lg" bg="dark:dark-700 light-100" /> -->
    <slot />
  </Hako>
</template>

<script setup>
import { Hako } from 'vue-hako'
import sizes from '/data/screen-sizes.json'
const size = ref('Moto 4G')
const width = computed(() => sizes[size.value][0])
const height = computed(() => sizes[size.value][1])
console.log(sizes);

</script>
<style lang="scss" scoped>
.tools {
  display: flex;
  justify-content: flex-end;
}
</style>
