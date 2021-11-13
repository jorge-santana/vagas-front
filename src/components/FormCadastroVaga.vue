<template>
  <form>
    <div class="mb-3">
      <label class="form-label">Título da Vaga</label>
      <input type="text" class="form-control" v-model="titulo">
      <div class="form-text">Por exemplo: Programador PHP Pleno.</div>
    </div>
    <div class="mb-3">
      <label class="form-label">Descrição</label>
      <textarea class="form-control" v-model="descricao"></textarea>
      <div class="form-text">Informe os detalhes da vaga.</div>
    </div>
    <button type="submit" class="btn btn-primary" @click.prevent="salvar()">Cadastrar</button>
  </form>
  {{vagas}}
</template>

<script>
// import EventBus from '@/EventBus'

export default {
  name: 'formCadastroVaga',
  data: () => ({
    titulo: '',
    descricao: '',
    vagas: JSON.parse(localStorage.getItem('vagas'))
  }),
  methods: {
    salvar () {
      this.vagas.push({
        titulo: this.titulo,
        descricao: this.descricao
      })
      localStorage.setItem('vagas', JSON.stringify(this.vagas))
      this.emitter.emit('alertar', {
        titulo: 'Cadastro',
        descricao: `A vaga <strong>${this.titulo}</strong> foi cadastrada com sucesso!`,
        tipo: 'sucesso'
      })
      this.resetaForm()
    },
    resetaForm () {
      this.titulo = ''
      this.descricao = ''
    }
  }
}
</script>

<style>

</style>
