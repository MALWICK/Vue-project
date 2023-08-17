<template>
  <div class="header">
    <h1>{{ title }}</h1>
    <AddButton
      @btn-click="$emit('toggle-add-task')"
      :text="showAddTask ? 'Close' : 'Add Task'"
      :color="showAddTask ? 'red' : 'green'"
    />
  </div>
</template>

<script>
import AddButton from './Button.vue'


export default {
  name: 'My-Header',
  props: {
    title: String,
    showAddTask: Boolean
  },
  components: {
    AddButton
  },
}
</script>

<style scoped>
.header {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
</style>
   
