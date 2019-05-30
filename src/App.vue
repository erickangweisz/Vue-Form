<template>
  <div id="app">
    <div class="container">
      <img alt="Vue logo" src="./assets/logo.png">
      <Home/>
    </div>
  </div>
</template>

<script>
import Home from './components/Home.vue'

export default {
  name: 'app',
  components: {
    Home
  }
}
</script>

<style>
#app {
  text-align: center;
  margin-top: 60px;
}
</style>
