<template>
  <div class="my-task" :key="task.id" v-for="task in tasks">
    <Task
      @toggle-reminder="$emit('toggle-reminder', task.id)"
      @delete-task="$emit('delete-task', task.id)"
      :task="task"
    />
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
    Task,

  },
  emits: ['delete-task', 'toggle-reminder'],
}
</script>