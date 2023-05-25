
<template>
  <div>
    <ClientOnly fallback-tag="span">
      <Preview>
        <iframe width="100%" height="100%" :src="`./${path}?preview=true`" frameborder="0"></iframe>
      </Preview>
    </ClientOnly>
  </div>
</template>
<script setup>
const path = useRoute().query.priview_path
const count = ref(0)
const add = () => count.value++
</script>
<style>
.c {

}
</style>
