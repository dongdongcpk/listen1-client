<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <nav class="bar bar-tab">
      <a class="tab-item external active" href="#">
          <span class="icon icon-home"></span>
          <span class="tab-label">首页</span>
      </a>
      <a class="tab-item external" href="#">
          <span class="icon icon-star"></span>
          <span class="tab-label">收藏</span>
      </a>
      <a class="tab-item external" href="#">
          <span class="icon icon-settings"></span>
          <span class="tab-label">设置</span>
      </a>
  </nav>
  </div>
</template>

<script>
export default {
  name: 'hello',
  data () {
    return {
      msg: 'My Music Player'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
