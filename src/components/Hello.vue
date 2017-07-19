<template>
  <div class="hello">
    <search v-on:search="updateItems"></search>
    <h1>{{ msg }}</h1>
    <div class="list-block media-list">
      <ul>
        <li v-for="item in items" :key="item.id">
          <div class="item-content">
            <div class="item-inner">
              <div class="item-title-row">
                <div class="item-title">{{item.title}}</div>
              </div>
              <div class="item-subtitle">{{`${item.artist} - ${item.album}`}}</div>
            </div>
          </div>
        </li>
      </ul>
    </div>
    <footerMenu></footerMenu>
  </div>
</template>

<script>
export default {
  name: 'hello',
  data () {
    return {
      msg: 'My Music Player',
      items: []
    }
  },
  methods: {
    updateItems (items) {
      this.items = items
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
  text-align: center;
}
</style>
