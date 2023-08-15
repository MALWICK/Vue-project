<template>
 <div class="container">
 <Headers title="Task Tracker" />
 </div>
</template>

<script>
import Headers from './components/Header.vue';
export default {
  name: 'App',
  components: {
  Headers,
  }
}
</script>

<style scoped>

@media (min-width: 1024px) {
}
</style>
