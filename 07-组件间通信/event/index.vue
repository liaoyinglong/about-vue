<template>
  <div>
    <div>
      父组件的data：{{num}}
    </div>
    <hr>
    <child :num='num' @add='addNum'></child>
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
      num: 10,
    }
  },
  methods: {
    addNum() {
      this.num++
    },
  },
}
</script>

