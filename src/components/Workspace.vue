<template>
  <div class="board-main-content">
    <BoardHeader v-bind="workspace" />
    <BoardCanvas />
  </div>
</template>

<script>
import BoardCanvas from './BoardCanvas.vue'
import BoardHeader from './BoardHeader.vue'

export default {
  name: 'Workspace',
  data() {
    return {
      workspace: {
        title: 'Production Workflow',
        users: ['Kevin Ruffin', 'Mikey Davidson', 'Paul Liebgott']
      }
    }
  },
  components: {
    BoardCanvas,
    BoardHeader
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
