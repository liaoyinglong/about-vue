<template>
  <div>
    <div>
      父组件的data：{{obj.num}}
    </div>
    <hr>
    <child :obj='obj'></child>
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
      obj: {
        num: 40,
      },
    }
  },
}
</script>

