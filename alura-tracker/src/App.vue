<template>
  <main class="columns is-gapless is-multiline">
    <div class="column is-one-quarter">
      <BarraLateralComponent />
    </div>

    <div class="column is-three-quarter">
      <FormularioComponent/>
    </div>

  </main>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import BarraLateralComponent from './components/BarraLateralComponent.vue';
import FormularioComponent from './components/FormularioComponent.vue';


export default defineComponent({
    name: 'App',
    components: { BarraLateralComponent, FormularioComponent }
});
</script>

<style>
</style>
