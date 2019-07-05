<template>
  <div id="app">
    <NavBar v-bind="currentUser" />
    <Workspace />
  </div>
</template>

<script>
import NavBar from './components/NavBar.vue'
import Workspace from './components/Workspace.vue'

export default {
  name: 'app',
  data() {
    return {
      currentUser: {
        username: 'kevinruffin1992',
        firstName: 'Kevin',
        lastName: 'Ruffin'
      }       
    }
  },
  components: {
    NavBar,
    Workspace
  }
}
</script>

<style>
</style>
