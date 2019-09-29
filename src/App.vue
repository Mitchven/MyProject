<template>
  <div id="app">
  <Header v-show = "$route.path === '/Login' || $route.path === '/Register'|| $route.path === '/' ? true: false"></Header>
  <AppBody></AppBody>
  <Sidebar v-show = "$route.path === '/Dashboard'">
  </Sidebar>
  </div>
</template>

<script>
import Sidebar from 'router/frame/Sidebar.vue'
import Header from 'router/frame/Header.vue'
import AppBody from 'router/frame/Body.vue'

export default {
  name: 'app',
  components: {
    Header,
    AppBody,
    Sidebar
  }
}
</script>
<style scoped>
</style>