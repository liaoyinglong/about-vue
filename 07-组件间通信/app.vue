<template>
  <div>
    <h2>组件通信</h2>
    <ol>
      <li @click='currentView = "event"'>event up, props down.父组件通过props向子组件传递数据，子组件通过$emit向上派发事件，父组件监听子组件派发的事件从而更改props传的值</li>
      <li @click='currentView = "bus"'>官方推荐的用一个空的vue示例来做中央事件处理。本质也是通过派发事件然后监听事件</li>
      <li @click='currentView = "parent"'>在子组件中通过$parent访问到父组件实例，从而更改父组件的数据</li>
      <li @click='currentView = "objectC"'>利用js中引用数据类型特性</li>
      <li>使用vuex来统一管理公共数据</li>
    </ol>
    <h3>当前组件【{{currentView}}】组件</h3>
    <component :is="currentView" style="margin-top:50px"></component>

  </div>
</template>

<script>
import event from './event'
import bus from './bus'
import parent from './parent'
import objectC from './object'
export default {
  components: { event, bus, parent, objectC },
  data() {
    return {
      currentView: 'event',
    }
  },
  methods: {},
}
</script>
<style>
body {
  font-size: 18px;
}
li {
  cursor: pointer;
  margin-bottom: 20px;
}
</style>
