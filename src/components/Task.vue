<template>
    <div :class="[task.reminder ? 'reminder':'','task']">
        <h3 class="My-task">{{ task.text }}
            <p  @click="onDelete(task.id)" class="fas">x</p>
        </h3>
        <p>{{ task.day }}</p>
    </div>
</template>

<script>
export default {
    name: 'My-Task',
    props: {
       task: Object, 
    },methods:{
        onDelete(id) {
            console.log(id)
        }
    }
}
</script>

<style scoped>
.task {
    background: #f4f4f4;
    margin: 5px;
    padding: 10 20px;
    cursor: pointer;
}

.fas {
    width: 30px;
    text-align: center;
    background-color: red;
    color: black;
    border: none;
    border-radius: 0.3rem;
}

.task.reminder {
    border-left: 5px solid green;
}

.task h3 {
    display: flex;
    align-items: center;
    justify-content: space-between;
}
</style>