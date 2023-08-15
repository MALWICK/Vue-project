<template>
  <div class="header" >
    <h1>{{ title }}</h1>
    <AddButton text="Add Task" color="green" />
  </div>
</template>

<script>
import AddButton from './Button.vue'

export default {
    name: 'My-Header',
    props:{ 
        title: String
    },
    components: {
       AddButton
    }
}
</script>

<style scoped>
 .header {
      display: flex;
      align-items: center;
      justify-content: center;  
    }
</style>
   
