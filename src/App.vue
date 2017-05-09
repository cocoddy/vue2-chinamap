<template>
  <div id="app">
    <area-map :tipFormater="tipFormater"></area-map>
  </div>
</template>

<script>
import areaMap from './components/map/areaMap.vue'
export default {
  name: 'app',
  components: {
    areaMap
  },
  methods: {
    tipFormater (params) {
          return `<p style="color:orange">${params.name}</p>`;
    }
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
