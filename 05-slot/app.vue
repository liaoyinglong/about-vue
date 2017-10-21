<template>
  <div>
    child组件
    <child :list='list'>
      <template slot-scope="scope">
        <span>{{scope.row.name}}---{{scope.row.age}}</span>
      </template>
    </child>
    <hr> 标签内没有写任何东西的 child组件
    <child :list='list'></child>
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
      list: [{ name: 'a', age: 18 }, { name: 'b', age: 19 }, { name: 'c', age: 20 }, { name: 'd', age: 21 }],
    }
  },
}
</script>