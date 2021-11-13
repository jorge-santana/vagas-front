<template>
    <div :class="classe">
      <h5>{{titulo}}</h5>
      <p v-html="descricao"></p>
    </div>
</template>

<script>
export default {
  name: 'Alerta',
  props: ['titulo', 'descricao', 'tipo'],
  computed: {
    classe () {
      switch (this.tipo) {
        case 'sucesso': return 'alert alert-success'
        default: return 'alert alert-primary'
      }
    }
  }
}
</script>

<style scoped>
.alert {
  position: absolute;
  right: 5px;
  top: 50px;
  z-index: 10
}
</style>
