<template>
  <ul>
    <li v-for="(item,index) in list" :key="index">
      <slot :row='item'>
        如果没有写任何东西就显示这个 -- {{index}}
      </slot>
    </li>
  </ul>
</template>
<script>
export default {
  props: ['list'],
}
</script>

