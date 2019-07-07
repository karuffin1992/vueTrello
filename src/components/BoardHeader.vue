<template>
  <div class="board-header">
    <b-navbar type="light" variant="info">
      <b-navbar-nav>
        <b-nav-item href="#">{{ title }}</b-nav-item>
      </b-navbar-nav>
    </b-navbar>
  </div>
</template>

<script>
export default {
  name: 'BoardHeader',
  props: {
    title: String,
    users: Array
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
</style>
