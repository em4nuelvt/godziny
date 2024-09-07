<!-- ---------------------------------------------------------------------- -->
<!-- HTML                                                                   -->
<!-- ---------------------------------------------------------------------- -->
<template>
  <div class="container py-4">
    <div class="row">
      <div class="col">
        <h2 class="text-secondary">Nova Categoria</h2>
      </div>
      <div class="h-100 p-5 bg-light border rounded-3">
        <form>
          <div class="mb-3">
            <label for="nome" class="form-label">Nome</label>
            <div class="input-group">
              <input type="text" class="form-control" id="nome" aria-describedby="basic-addon3 basic-addon4" required >
            </div>
          </div>
          <div class="mb-3">
            <label for="descricao" class="form-label">Descrição</label>
            <div class="input-group">
              <textarea class="form-control" id="descricao" aria-label="With textarea" required ></textarea>
            </div>
          </div>
          <div class="mb-3">
            <label for="max-horas" class="form-label">Número Máximo de horas</label>
            <div class="input-group">
              <input type="text" class="form-control" id="max-horas" required >
            </div>
          </div>
          <div class="mb-3">
            <label for="multiplicador" class="form-label">Multiplicador de Horas</label>
            <div class="input-group">
              <input type="text" class="form-control" id="multiplicador" required >
            </div>
          </div>
          <div class="row">
            <div class="col d-flex justify-content-end">
              <button type="submit" class="btn btn-primary text-white">Adicionar</button>
            </div>
          </div>
        </form>
      </div>
    </div>
  </div>
</template>


<!-- ---------------------------------------------------------------------- -->
<!-- JavaScript                                                             -->
<!-- ---------------------------------------------------------------------- -->
<script setup>
</script>

<!-- ---------------------------------------------------------------------- -->
<!-- CSS                                                                    -->
<!-- ---------------------------------------------------------------------- -->
<style scoped>
* {
  color: #464545;
}
</style>