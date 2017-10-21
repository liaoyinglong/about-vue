<template>
  <div>
    <button @click="changeView">切换显示组件</button>
    <component :is="currentView"></component>
  </div>
</template>

<script>
import childA from './childA'
import childB from './childB'
export default {
  components: {
    childA,
    childB,
  },
  data() {
    return {
      currentView: 'childA',
    }
  },
  methods: {
    changeView() {
      this.currentView = this.currentView === 'childA' ? 'childB' : 'childA'
    },
  },
}
</script>