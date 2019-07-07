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
  components: {
    NavBar,
    Workspace
  },
  data() {
    return {
      currentUser: {
        username: 'kevinruffin1992',
        firstName: 'Kevin',
        lastName: 'Ruffin'
      }       
    }
  }
}
</script>

<style>
</style>
