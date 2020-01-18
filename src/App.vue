<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png"/>
    <div class="container">
      <div class="row">
        <Card/>
        <Card/>
        <Card/>
        <Card/>
        <Card/>
        <Card/>
      </div>
    </div>
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import Card from './components/Card.vue'

export default {
  name: 'app',
  data(){
    return {
      hello: "world",
      style: 'color: red;',
      posts : [{
          title : '오늘의 일기',
          date : '4월 20일'
        }, {
          title : '수분크림 추천',
          date : '3월 4일'
        }, {
          title : '강남 맛집 후기',
          date : '2월 22일'
        }
      ],
    }
  },
  components: {
    // HelloWorld
    Card: Card,
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
