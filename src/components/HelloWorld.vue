<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <div class="time">{{date}}</div>
  </div>
</template>

<!-- 注意： link 不能使用，因为它是内置的标签
       你要使用另外一个名称就行了，一般加上一个前缀
     -->
<div>
<span>{{ newDate }}</span>
</div>
<script>

export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  name1: 'test',
  data: function () {
    return {
      date: new Date()
    }
  },
  created () {
  },
  mounted () {
    const that = this
    this.timer = setInterval(function () {
      that.date = new Date().toLocaleString()
    })
  },
  methods: {}
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h3 {
  margin: 40px 0 0;
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
div{
  border: 1px solid black;
}
</style>
