<template>
  <div>
    父组件传递过来的data:{{obj.num}}
    <br>
    <button @click="handleAddButton">子组件按钮-点击父组件数据+1</button>
  </div>
</template>

<script>
export default {
  props: ['obj'],
  methods: {
    handleAddButton() {
      this.obj.num++
    },
  },
}
</script>
