<template>
  <li @click="handleClick" class="item">
    {{content}}
  </li>
</template>

<script>
export default {
  props: ['content', 'index'],
  methods: {
    handleClick () {
      this.$emit('delete', this.index)
    }
  }
}
</script>

<style scoped>
    .item {
        color: red;
    }
</style>
