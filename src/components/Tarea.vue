<template>
  <h1>App Tareas</h1>
  <TareaForm />
  <TareaItem 
    v-for="tarea in tareas" :key="tarea.id"
    :tarea="tarea"
  />
  <div class="alert alert-dark mt-3" v-if="tareas.length===0">Sin Tareas Pendientes 🤷‍♂️ </div>
  <p>{{ tareas }}</p>
</template>

<script>
import { provide, ref } from 'vue'
import TareaForm from './TareaForm.vue';
import TareaItem from './TareaItem.vue';

export default {
    components: { TareaForm, TareaItem },
    setup() {
        const tareas = ref([]);

        provide('tareas', tareas)

        return { tareas };
    }
}
</script>

<style>

</style>