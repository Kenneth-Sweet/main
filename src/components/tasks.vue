<template>
<div>
    <div :key="task.id" v-for="task in tasks">
        <MyTask @delete-MyTask="$emit('delete-MyTask', task.id)" :task="task"></MyTask>

    </div>
    </div>
</template>


<script>


import MyTask from './task'



export default {
    name: 'MyTasks',
    props: {
        tasks: Array,
    },
    components: {
        MyTask
    },
    emits: ['delete-MyTask']
}


</script>
