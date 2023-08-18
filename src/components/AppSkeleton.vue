<template>
  <div class="container">
    <AnimatedPlaceholder width="100%" height="80%" />
    <div>
      <Headers @toggle-add-task="toggleAddTask" title="Task Tracker" :showAddTask="showAddTask" />

      <AnimatedPlaceholder width="100%" height="100px" />
    </div>
    <AnimatedPlaceholder width="100%" height="80%" />
    <div v-show="showAddTask">
      <AddTask @add-task="addTask" />
      <AnimatedPlaceholder width="100%" height="100px" />
      <AnimatedPlaceholder width="36px" height="20px" />
    </div>
    <AnimatedPlaceholder width="36px" height="20px" />
    <AnimatedPlaceholder width="36px" height="20px" />
    <AnimatedPlaceholder width="36px" height="20px" />
    <AnimatedPlaceholder width="36px" height="20px" />
    <div>
      <Tasks @toggle-reminder="toggleReminder" @delete-task="deleteTask" v-bind:tasks="tasks" />
      <AnimatedPlaceholder width="100%" height="100px" />
    </div>
    <div class="summary-placeholder"></div>
  </div>
</template>

<script>
import AnimatedPlaceholder from './AnimatedPlaceholder.vue'

export default {
  components: { AnimatedPlaceholder }
}
</script>

<style scoped>
.summary-placeholder {
  display: flex;
  flex-direction: column;
  gap: 8px;
  width: 100%;
}
</style>

