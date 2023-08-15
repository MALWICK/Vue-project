<template>
  <div class="container">
    <Headers title="Task Tracker" />
  </div>
</template>

<script>
import Headers from './components/Header.vue'
export default {
  name: 'App',
  components: {
    Headers
  },
  data() {
    return {
      tasks: [],
    }
  }
}
</script>

<style scoped>
.container {
  max-width: 500px;
  margin: 30px auto;
  overflow: auto;
  min-height: 300px;
  border: 1px solid steelblue;
  padding: 30px;
  border-radius: 5px;
}

.btn {
  display: inline-block;
  background: #000;
  color: #fff;
  border: none;
  padding: 10px 20px;
  margin: 5px;
  border-radius: 5px;
  cursor: pointer;
  text-decoration: none;
  font-size: 15px;
  font-family: inherit;
}

.btn:focus {
  outline: none;
}

.btn:active {
  transform: scale(0.98);
}

.btn-block {
  display: block;
  width: 100%;
}

@media (min-width: 1024px) {
}
</style>
