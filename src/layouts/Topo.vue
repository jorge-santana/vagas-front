<template>
  <nav class="navbar navbar-expand-lg navbar-dark bg-dark" aria-label="Eighth navbar example">
    <div class="container">
      <a class="navbar-brand" href="#">Jorge Sant Ana</a>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarsExample07" aria-controls="navbarsExample07" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>

      <div class="collapse navbar-collapse" id="navbarsExample07">
        <ul class="navbar-nav me-auto mb-2 mb-lg-0">
          <li class="nav-item">
            <a class="nav-link" href="#home" @click="selecionar('Home')">Home</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#publicar-vaga" @click="selecionar('PublicarVaga')">Publicar Vaga</a>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'Topo',
  methods: {
    selecionar (c) {
      this.$emit('mudarConteudo', c)
    }
  }
}
</script>

<style>

</style>
