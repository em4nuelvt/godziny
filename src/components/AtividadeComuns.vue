<template>
  <div class="card">
      <ul class="list-group list-group-flush">
          <li class="list-group-item"><strong>Título:</strong> {{ titulo }}</li>
          <li class="list-group-item"><strong>Categoria:</strong> {{ categoria.nome }}</li>
          <li class="list-group-item"><strong>Arquivo:</strong> {{ fileName }}</li>
          <li class="list-group-item"><strong>Data e Hora:</strong> {{ formattedDataHora }}</li>
          <li class="list-group-item"><strong>Status:</strong> {{ status }}</li>
      </ul>
  </div>
</template>

<script setup>
import { defineProps, computed } from 'vue';

// Recebe os valores via props enviados pelo componente pai
const props = defineProps({
titulo: {
  type: String,
  required: true
},
categoria: {
  type: Object,
  required: true
},
file: {
  type: Object, // Use Object para aceitar File
  required: true
},
createdAt: {
  type: [String, Date], // Aceita String ou Date
  required: true
},
status: {
  type: String,
  required: true
},
});

// Computed para extrair o nome do arquivo
const fileName = computed(() => {
return props.file ? props.file.name : 'Nenhum arquivo selecionado';
});

// Computed para formatar a data e hora
const formattedDataHora = computed(() => {
if (!props.createdAt) return 'Data e hora não especificadas';
const date = new Date(props.createdAt);
return date.toLocaleString(); // Formata a data e hora conforme as configurações locais
});
</script>

<style scoped>
.card {
margin: 1rem;
}
.list-group-item {
font-size: 1rem;
}
</style>
