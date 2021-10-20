<template>
  <div>
    <Topo />
    <Home />
  </div>
</template>

<script>
import Home from './views/Home.vue'
import Topo from './layouts/Topo.vue'

export default {
  name: 'App',
  components: {
    Home,
    Topo
  }
}
</script>

<style>

</style>
