<template>
  <div class="f-menu">
    <ul>
      <li :class="{ active: route.query.priview_path == item.name }" v-for="item in menu">
        <nuxt-link :to="{ path: '/preview', query: { priview_path: item.name } }">{{ item.name }}</nuxt-link>
      </li>
    </ul>
  </div>
</template>
<script setup>
const route = useRoute()
const menu = [
  {
    path: '/header',
    name: 'header',
  },
  {
    path: '/menu',
    name: 'menu',
  },
]

</script>
<style lang="scss">
.f-menu {
  width: 150px;

  ul {
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

    li {
      height: 40px;
      padding: 0 10px;
      box-sizing: border-box;
      line-height: 40px;
      cursor: pointer;
      border-bottom: 1px solid rgb(226 232 240 / 80%);

      &:last-child {
        border-bottom: none;
      }

    }

    .active {
      color: #3C72ED;
      font-weight: 700;
    }
  }
}
</style>
