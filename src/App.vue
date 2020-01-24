<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png"/>
    <div class="container">
    <button v-on:click="sort_price()" class="btn btn-danger"> sort by price</button>
    <button v-on:click="sort_name()" class="btn btn-danger"> sort by name</button>
    <button v-on:click="sort_reset()" class="btn btn-danger"> reset </button>
    </div>
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
  },
  methods: {
    sort_price(){
      this.data.sort(function(a, b){
        return a.price - b.price;
      })
    },
    sort_name(){
      this.data.sort(function(a, b){
        return (a.title < b.title) ? -1 : (a.title > b.title) ? 1 : 0;
      });
    },
    sort_reset(){
      this.data.unshift();
    },
  },
  computed: {

  }, watch: {

  },
  created(){

  },
  mounted(){

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
