<template>
  <div class="my-task" :key="task.id" v-for="task in tasks">
    <Task @delete-task="$emit('delete-task', task.id)" :task="task "/>
  </div>
</template>

<script>
import Task from './Task.vue'
export default {
  name: 'My-Tasks',
  props: {
    tasks: Array
  },

  components: {
    Task
  }
}
</script>