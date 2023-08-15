<template>
  <div class="container">
    <Headers title="Task Tracker" />
    <Tasks :tasks="tasks"/>
  </div>
</template>

<script>

import Headers from './components/Header.vue'
import Tasks from './components/Tasks.vue'

export default {
  name: 'App',
  components: {
    Headers,
    Tasks,
  },
  data() {
    return {
      tasks: [],
    }
  },
  created() {
    this.tasks = [
      {
        id: 1,
        text: 'Learn Vue',
        day: 'March 1st at 2:30pm',
        reminder: true
      },
      {
        id: 2,
        text: 'Meet at school',
        day: 'March 2nd at 2:00pm',
        reminder: false,
      },
      {
        id: 3,
        text: 'Buy Groceries',
        day: 'March 3rd at 12:30pm',
        reminder: true
      },
      {
        id: 4,
        text: 'Learn Vue',
        day: 'March 4th at 10:30am',
        reminder: false
      },
      {
        id: 5,
        text: 'Take out the the dog for a walk',
        day: 'March 5th at 1:00pm',
        reminder: true
      },
      {
        id: 6,
        text: 'Visit grand Mom',
        day: 'March 6th at 2:00pm',
        reminder: false
      }
    ]
  }
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400&display=swap');
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
