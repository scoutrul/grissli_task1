<template>
  <div id="app">
    <h1>Бутылочка</h1>
    <Bottle :fillIn="+fillIn" :fillOut="+fillOut"/>
    <input v-model="fillIn" placeholder="Наполннить" type="number">
    <input v-model="fillOut" placeholder="Слить" type="number">
  </div>
</template>

<script>
import Bottle from './components/Bottle.vue'

export default {
  name: 'app',
  components: {
    Bottle
  },
  data: () => ({
    fillIn: 0,
    fillOut: 0
  })
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
