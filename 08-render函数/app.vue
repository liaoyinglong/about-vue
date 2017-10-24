<template>
  <div>
    
  </div>
</template>

<script>
export default {
  components: {},
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