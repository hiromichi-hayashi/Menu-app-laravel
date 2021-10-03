<template>
  <div class="app">
    <Layout>
      <Side />
    </Layout>
  </div>
</template>

<script>
import Layout from './layout/layout.vue'
import Side from './parts/Side.vue'

export default {
  name: 'App',
  components: {
    Layout,
    Side,
  }
}
</script>
<style lang="scss">
</style>