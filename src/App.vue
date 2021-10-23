<template>
  <div>
    <Topo @mudarConteudo="view = $event" />
    <Conteudo :componente="view" />
  </div>
</template>

<script>
import Conteudo from './layouts/Conteudo.vue'
import Topo from './layouts/Topo.vue'

export default {
  name: 'App',
  data: () => ({
    view: 'Home'
  }),
  components: {
    Conteudo,
    Topo
  }
}
</script>

<style>

</style>
