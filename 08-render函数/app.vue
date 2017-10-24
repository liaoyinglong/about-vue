<template>
  <div>
    <headerComponent v-for="item in 6" :level='item' msg='hello' :key="item"></headerComponent>
  </div>
</template>

<script>
import headerComponent from './headerComponent'
export default {
  components: { headerComponent },
}
</script>