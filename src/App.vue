<template>
  <div id="app">
    <Layout></Layout>
  </div>
</template>

<script>
import Layout from './components/Layout.vue'
export default {
  name: 'app',
  components: {
    Layout
  }
}
</script>


<style scoped>

#app {
  display: flex;
  flex: 1;
  height: 100%;
}

</style>