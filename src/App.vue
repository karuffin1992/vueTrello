<template>
  <div id="app">
    <NavBar />
    <Workspace />
  </div>
</template>

<script>
import NavBar from './components/NavBar.vue'
import Workspace from './components/Workspace.vue'

export default {
  name: 'app',
  components: {
    NavBar,
    Workspace
  }
}
</script>

<style>
</style>
