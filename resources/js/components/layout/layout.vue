<template>
  <div class="app">
    <Header class="no_flex"></Header>
    <slot></slot>
  </div>
</template>

<script>
import Header from '../parts/Header.vue'
export default {
  name: 'layout',
  components: {
    Header
  }
}
</script>

<style lang="scss" scoped>
</style>