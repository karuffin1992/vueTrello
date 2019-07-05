<template>
  <div class="board-main-content">
    <BoardHeader />
    <BoardCanvas />
  </div>
</template>

<script>
import BoardCanvas from './BoardCanvas.vue'
import BoardHeader from './BoardHeader.vue'

export default {
  name: 'Workspace',
  components: {
    BoardCanvas,
    BoardHeader
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
