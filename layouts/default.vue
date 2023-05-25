<template>
  <div class="app">
    <FHeader v-show="!istrue"/>
    <div class="content mw">
      <FMenu v-show="!istrue"/>
      <div class="page">
        <NuxtPage />
      </div>
    </div>
    <FFooter v-show="!istrue" />
  </div>
</template>
<script setup>
const istrue = useRoute().query?.preview
</script>
<style lang="scss">
.app {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  box-sizing: border-box;

  .content {
    width: 100%;
    margin-top: 15px;
    flex: 1;
    display: flex;
    justify-content: flex-start;

    .page {
      flex: 1;
      margin: 0 10px;
      padding: 10px;
      background-color: #ffffff;
      display: -webkit-box;
      display: -webkit-flex;
      display: -ms-flexbox;
      display: flex;
      -webkit-flex-direction: column;
      -ms-flex-direction: column;
      flex-direction: column;
      overflow-y: auto;
      overflow-x: hidden;
      border-radius: 0.5rem;
      border-width: 1px;
      border: 1px solid;
      border-color: rgb(226 232 240 / 80%);
      color: rgb(15 23 42 / 1);
      height: auto;
    }
  }
}
</style>
