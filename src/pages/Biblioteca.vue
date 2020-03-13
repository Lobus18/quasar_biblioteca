<template>
  <q-page class="bg-grey-3 q-pa-lg">
    <q-list class="bg-white"
    separator
    bordered
    >
      <q-item 
      v-for="task in tasks"
      :key="task.titulo"
      v-ripple>
        <q-item-section avatar>
          <q-checkbox v-model="task.done" color="primary" />
        </q-item-section>
        <q-item-section>
          <q-item-label>{{task.titulo}}</q-item-label>
        </q-item-section>
      </q-item>
    </q-list>
  </q-page>
</template>

<script>
export default {
  data(){
    return{
      tasks: [
        {
          titulo: 'Livro de Matematica',
          done: false
        },
        {
          titulo: 'Livro de Portugues',
          done: false
        },
        {
          titulo: 'Livro de Artes',
          done: false
        }
      ]
    }
  }
};
</script>
