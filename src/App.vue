<template>
  <div id="app">
    <HelloWorld />
    <SideBar />
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import SideBar from './components/SideBar.vue'

export default {
  name: 'app',
  components: {
    HelloWorld,
    SideBar
  }
}
</script>

<style>
#app {
  display: flex;
  flex-direction: column;
}
</style>
