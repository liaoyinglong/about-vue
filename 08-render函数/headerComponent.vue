<script>
export default {
  props: ['level', 'msg'],
  render(h) {
    const tag = `h${this.level}`
    return h(tag, this.msg)
  },
}
</script>
