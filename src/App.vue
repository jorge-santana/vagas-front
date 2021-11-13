<template>
  <div>
    <Topo @mudarConteudo="view = $event" />
    <Alerta :titulo="alerta.titulo"
      :descricao="alerta.descricao"
      :tipo="alerta.tipo"
      v-show="alertaVisivel"
    />
    <Conteudo :componente="view" />
  </div>
</template>

<script>
import Alerta from './components/Alerta.vue'
import Conteudo from './layouts/Conteudo.vue'
import Topo from './layouts/Topo.vue'

export default {
  name: 'App',
  data: () => ({
    view: 'Home',
    alerta: { titulo: '', descricao: '', tipo: '' },
    alertaVisivel: false
  }),
  components: {
    Alerta,
    Conteudo,
    Topo
  },
  methods: {
    exibeOcultaAlerta () {
      this.alertaVisivel = !this.alertaVisivel
    }
  },
  mounted () {
    this.emitter.on('alertar', alerta => {
      this.alerta = alerta
      this.exibeOcultaAlerta()
      setTimeout(this.exibeOcultaAlerta, 5000)
    })
  }
}
</script>

<style>

</style>
