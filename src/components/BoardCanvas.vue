<template>
    <div class="board-canvas">
      <BoardList />
    </div>
</template>

<script>
import BoardList from './BoardList.vue'

export default {
  name: 'BoardCanvas',
  components: {
    BoardList
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
