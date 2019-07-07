<template>
    <div class="board-list">
      <div class="list-wrapper" v-if="isIdle">
        <b-form class="add-list-btn" v-if="addList">
          <b-form-input
            id="0"
            title=""
          />
          <b-button type="submit" variant="primary">Submit</b-button>
          <b-button type="reset" variant="danger">Discard</b-button>
        </b-form>
        <b-button block :pressed.sync="addList">+ Add a List</b-button>
      </div>
      <div class="list-wrapper" v-else>
        <BoardCard v-for="card in cards" 
          v-bind:key="card.id"
          v-bind:title="card.title"
        />
      </div>
    </div>
</template>

<script>
import BoardCard from './BoardCard.vue'

export default {
  name: 'BoardList',
  components: {
    BoardCard    
  },
  data() {
    return {
      cards: [],
      isIdle: true,
      addList: false
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.add-list-btn {
  padding-bottom: 5px;
}

.list-wrapper {
  width: 300px; 
  margin: 10px 10px 10px 10px;
  min-height: 40px;
}
</style>
