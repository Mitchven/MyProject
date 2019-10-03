<template>
  <div id="app">
  <Header></Header>
  <AppBody></AppBody>
  </div>
</template>

<script>
import Header from 'router/frame/Header.vue'
import AppBody from 'router/frame/Body.vue'

export default {
  name: 'app',
  components: {
    Header,
    AppBody
  }
}
</script>
