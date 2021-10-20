<template>
    <div :class="classe">
      <p>{{titulo}}</p>
      <h2>{{total}}</h2>
    </div>
</template>

<script>
export default {
  name: 'Indicador',
  props: ['titulo', 'total', 'bg', 'color'],
  computed: {
    classe () {
      return `h-100 p-5 rounded-3 border ${this.bg} ${this.color}`
    }
  }
}
</script>

<style scoped>

</style>
