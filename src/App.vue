<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png"/>
    <div class="container">
      <div class="row">
        <Card v-for="item in data" v-bind:item="item" :key=item></Card>
      </div>
    </div>
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import Card from './components/Card.vue'
import data from './assets/data.js'

export default {
  name: 'app',
  data(){
    return {
      data: data,
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
