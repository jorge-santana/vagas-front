<template>
  <div>
    <div class="container py-4">
      <div class="row">
        <div class="col">
          <h4>Apresente a sua vaga para milhares de profissional e de graça!</h4>
          <hr />
          <form-cadastro-vaga />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import FormCadastroVaga from '@/components/FormCadastroVaga.vue'

export default {
  name: 'PublicarVaga',
  components: {
    FormCadastroVaga
  }
}
</script>

<style>

</style>
