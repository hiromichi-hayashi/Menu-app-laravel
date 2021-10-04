<template>
  <div class="app">
    <Layout>
      <div class="flex">
        <Side />
        <Content />
      </div>
    </Layout>
  </div>
</template>

<script>
import Layout from './layout/layout.vue'
import Side from './parts/Side.vue'
import Content from './parts/Content.vue'

export default {
  name: 'App',
  components: {
    Layout,
    Side,
    Content,
  }
}
</script>
<style lang="scss" scoped>

.flex {
  display: flex;
  @media screen and (max-width: 767px) {
    display: block;
  }
}
</style>