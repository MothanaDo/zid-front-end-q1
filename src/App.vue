<template>
  <div id="app">
    <SideMenu />
    <Home />
  </div>
</template>

<script>
import Home from './components/Home.vue'
import SideMenu from './components/SideMenu.vue'
export default {
  name: 'App',
  components: {
    Home,SideMenu
  }
}
</script>

<style>
#app {

}
</style>
