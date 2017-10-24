<template>
  <div>
    <div>
      父组件的data：{{num}}
    </div>
    <hr>
    <child :num='num'></child>
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
      num: 30,
    }
  }
}
</script>

