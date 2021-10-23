<template>
  <div>
    <div class="container py-4">
      <div class="row">
        <div class="col">
          <PesquisaVagas />
        </div>
      </div>
      <div class="row mt-5">
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

export default {
  name: 'Home',
  components: {
    Indicador,
    PesquisaVagas
  }
}
</script>

<style>

</style>
