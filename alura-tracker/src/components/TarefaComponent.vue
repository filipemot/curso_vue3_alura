<template>
    <Box>
      <div class="columns">
        <div class="column is-7">{{ tarefa.descricao || 'Tarefa sem descrição' }}</div>
        <div class="column">
          <CronometroComponent :tempoEmSegundos="tarefa.duracaoEmSegundos"/>
        </div>
      </div>
    </Box>
  </template>
  
  <script lang="ts">
  import { defineComponent, PropType } from "vue";
  import CronometroComponent from "./CronometroComponent.vue";

  import Box from './BoxComponent.vue'
  import ITarefa from '../interfaces/ITarefa';
  
  export default defineComponent({
    name: "TarefaComponent",
    components: {
      CronometroComponent,
      Box
    },
    props: {
      tarefa: {
        type: Object as PropType<ITarefa>,
        required: true
      }
    }
  });
  </script>