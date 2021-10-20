<template>
  <div class="h-100 p-5 bg-light border rounded-3">
    <h2>Pesquisar Vagas</h2>
    <form>
      <div class="row">
        <div class="col">
          <div class="form-group">
            <label>Título da vaga</label>
            <input type="text" class="form-control" placeholder="Palavras chaves, por exemplo 'PHP', 'Pleno', 'Analista'">
            <small id="emailHelp" class="form-text text-muted">Informe palavras que estejam relacionadas com o título da vaga que você procura</small>
          </div>
        </div>
      </div>
      <button class="btn btn-outline-dark mt-2" type="button">Buscar</button>
    </form>
  </div>
</template>

<script>
export default {
  name: 'PesquisaVagas'
}
</script>

<style scoped>

</style>
