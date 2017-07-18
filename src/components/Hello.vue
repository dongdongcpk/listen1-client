<template>
  <div class="hello">
    <search></search>
    <h1>{{ msg }}</h1>
    <footerMenu></footerMenu>
  </div>
</template>

<script>
export default {
  name: 'hello',
  data () {
    return {
      msg: 'My Music Player'
    }
  },
  components: {
    footerMenu: require('./menu.vue'),
    search: require('./search.vue')
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1 {
  font-weight: normal;
}
</style>
