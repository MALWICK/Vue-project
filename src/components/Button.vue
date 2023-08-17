<template>
    <div  class="button-holder">
<button @click="onClick()" class="My-add" :style="{ background : color }" type="button">{{ text }}</button>
    </div>
</template>

<script>
export default  {
    name: 'add-Button',
    props: {
        text: String,
        color: String,
    },
    methods:{
        onClick(){
           this.$emit('btn-click');
        }
    }
}
</script>

<style scoped>
.My-add {
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

.My-add:focus {
  outline: none;
}
</style>