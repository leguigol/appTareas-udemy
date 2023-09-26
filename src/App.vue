<template>
  <div class="container">
    <Tarea />
  </div>
</template>

<script>
import Tarea from './components/Tarea.vue';
import TareaItem from './components/TareaItem.vue';

export default {
  name: 'App',
  components: {
    Tarea,
    TareaItem
},
  setup(){
  }
}
</script>

