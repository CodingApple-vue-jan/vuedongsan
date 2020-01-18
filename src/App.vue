<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png"/> -->
    <div class="container">
      <div class="row">
        <div class="col-md-6">
          <div class="card" style="width: 18rem;">
            <img src="./assets/logo.png" class="card-img-top" alt="...">
            <div class="card-body">
              <h5 class="card-title">Card title</h5>
              <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
              <a href="#" class="btn btn-primary">Go somewhere</a>
            </div>
          </div>
        </div>
        <div class="col-md-6">item2</div>
      </div>
    </div>
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'

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
