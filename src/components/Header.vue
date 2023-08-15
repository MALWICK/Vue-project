<template>
  <div class="header" >
    <h1>{{ title }}</h1>
  </div>
</template>

<script>
export default {
    name: 'My-Header',
    props: ['title']
}
</script>

<style scoped>
 .header {
      display: flex;
      align-items: center;
      justify-content: center;  
    }
</style>
   
