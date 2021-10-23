<template>
  <div>
      <Home v-if="componente == 'Home'" />
      <PublicarVaga v-if="componente == 'PublicarVaga'" />
  </div>
</template>

<script>
import Home from '../views/Home.vue'
import PublicarVaga from '../views/PublicarVaga.vue'

export default {
  name: 'Conteudo',
  props: ['componente'],
  components: {
    Home,
    PublicarVaga
  }
}
</script>

<style>

</style>
