<template>
  <div>
    <div class="container py-4">
      <div class="row">
        <div class="col">
          <PesquisaVagas />
        </div>
      </div>

      <div class="row mt-3">
        <div class="col">
          <Vaga v-for="vaga, id in vagas" :key="id">
            <div class="card mb-3">
              <div class="card-header bg-success text-white">{{vaga.titulo}}</div>
              <div class="card-body">
                  {{vaga.descricao}}
              </div>
          </div>
          </Vaga>
        </div>
      </div>

      <div class="row mt-3">
        <div class="col-4">
          <Indicador titulo="Vagas abertas" total="100" bg="bg-dark" color="text-white" />
        </div>
        <div class="col-4">
          <Indicador titulo="Profissionais cadastrados" total="25" bg="bg-dark" color="text-white" />
        </div>
        <div class="col-4">
          <Indicador titulo="Visitantes online" total="10" bg="bg-light" color="" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Indicador from '@/components/Indicador.vue'
import PesquisaVagas from '@/components/PesquisaVagas.vue'
import Vaga from '@/components/Vaga.vue'

export default {
  name: 'Home',
  data: () => ({
    vagas: []
  }),
  components: {
    Indicador,
    PesquisaVagas,
    Vaga
  },
  mounted () {
    this.emitter.on('listarVagas', vaga => {
      const vagas = JSON.parse(localStorage.getItem('vagas'))
      this.vagas = vagas.filter(reg => reg.titulo.toLowerCase().includes(vaga.titulo.toLowerCase()))
    })
  }
}
</script>

<style>

</style>
