<template>
  <div>
    <input type="text" @input="handleInput($event)">
  </div>
</template>
<script>
export default {
  props: ['appValue'],
  methods: {
    handleInput(e) {
      this.$emit('update:appValue', e.target.value)
    },
  },
}
</script>
