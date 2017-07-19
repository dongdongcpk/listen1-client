<template>
  <div class="bar bar-nav">
    <div class="searchbar">
      <a class="searchbar-cancel">取消</a>
      <div class="search-input">
        <label class="icon icon-search" for="search"></label>
        <input type="search" id='search' placeholder='搜索音乐...' v-model="keywords"/>
      </div>
    </div>
  </div>
</template>

<script>
import axios from 'axios'

export default {
  data () {
    return {
      keywords: '',
      result: []
    }
  },
  methods: {
    search (keywords = '') {
      axios.get(`http://localhost:8888/search_hybrid?source=4&keywords=${keywords}`)
        .then(response => {
          this.result = response.data.result
          this.$emit('search', this.result)
        })
        .catch(error => {
          console.log(error)
        })
    }
  },
  watch: {
    keywords (newKeywords) {
      this.search(newKeywords)
    }
  }
}
</script>

