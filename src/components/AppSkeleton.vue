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
    </div>
    <AnimatedPlaceholder width="100%" height="80%" />
    <AnimatedPlaceholder width="100%" height="80%" />
    <AnimatedPlaceholder width="100%" height="80%" />
    <AnimatedPlaceholder width="100%" height="80%" />
  <div>
    <Tasks @toggle-reminder="toggleReminder" @delete-task="deleteTask" v-bind:tasks="tasks" />
        <AnimatedPlaceholder width="100%" height="100px" />
        <AnimatedPlaceholder width="100%" height="80%" />
  </div>
    <div class="summary-placeholder"></div>
  </div>
</template>

<script>
import AnimatedPlaceholder from './AnimatedPlaceholder.vue'


export default {
  components: { AnimatedPlaceholder },

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

