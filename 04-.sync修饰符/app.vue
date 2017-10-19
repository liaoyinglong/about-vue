<template>
  <div>
    <child :appValue.sync='appValue'></child>
    <!-- <child :appValue='appValue' @update:appValue='val=> appValue = val'></child> -->
    <br> child组件输入的value：{{appValue}}
  </div>
</template>

<script>
import child from './child'
export default {
  components: {
    child,
  },
  data() {
    return {
      appValue: '',
    }
  },
}
</script>