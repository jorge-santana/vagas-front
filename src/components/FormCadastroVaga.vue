<template>
  <form>
    <div class="mb-3">
      <label class="form-label">Título da Vaga</label>
      <input type="text" class="form-control">
      <div class="form-text">Por exemplo: Programador PHP Pleno.</div>
    </div>
    <div class="mb-3">
      <label class="form-label">Descrição</label>
      <textarea class="form-control"></textarea>
      <div class="form-text">Informe os detalhes da vaga.</div>
    </div>
    <button type="submit" class="btn btn-primary">Cadastrar</button>
  </form>
</template>

<script>
export default {
  name: 'formCadastroVaga'
}
</script>

<style>

</style>
