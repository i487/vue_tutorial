<template>
    <div :class=" [task.reminder ? 'reminder'  : '', 'task'] ">
        <h3 class="task__title"> {{task.text}} 
             <i @click="onDelete(task.id)" class="fas fa-times"></i>
        </h3>
       <p class="task__text">
           {{task.day}}
       </p>
    </div>
</template>

<script>
export default {
    name: "Task",
    props: {
        task: Object,
    },
    methods: {
        onDelete (id){
            this.$emit('delete-task', id)
        }
    }
}
</script>


<style>
    .task {
        background: #F4F4F4;
        margin: 5px;
        padding: 10px 20px;
        cursor: pointer;
    }
    .reminder {
        border-left: 5px solid green;

    }
    .task__title {
        display: flex;
        align-items: center;
        justify-content: space-between;
    }
    .fas {
        color: red;
    }
</style>