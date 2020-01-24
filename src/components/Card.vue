<template>
<div class="col-md-6">
  <div class="card" style="width: 18rem;">
    <img v-bind:src="item.image" class="card-img-top" />
      <div class="card-body">
        <h5 class="card-title">{{item.title}}</h5>
        <p class="card-text">{{item.caption}}</p>
        <p class="card-price">{{item.price}}</p>
        <a href="#" class="btn btn-primary">Go somewhere</a>
      </div>
  </div>
</div>
</template>

<script>
export default {
  props: {item: Object}
}
</script>

<style>

</style>