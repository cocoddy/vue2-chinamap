# vue2-chinamap

> This is an example of a map of China can drill data.

### QQ交流群:255965810

### How to run demo
```
npm install
npm run dev
```
### 效果图
 ![效果图](http://files.cnblogs.com/files/rohelm/vue-map.gif)
::: demo
```html
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

```
### props
| 参数      | 说明          | 类型      | 可选值                           | 默认值  |
|---------- |-------------- |---------- |--------------------------------  |-------- |
| tipFormater | 钻取级别数据提示格式化 | Function | 可以为空 | null |
| labelLevel | 默认文本开始显示层级，默认第一次不显示文本| Number | 可以为空 | 1 |
