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
import bus from './bus'
import child from './child'
export default {
  components: {
    child,
  },
  data() {
    return {
      num: 20,
    }
  },
  created() {
    bus.$on('add', () => {
      this.num++
    })
  },
}
</script>

