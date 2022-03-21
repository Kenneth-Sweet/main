<template>

<div  :class="[task.reminder ? 'reminder' : '', 'task']">
    <h3>{{task.text}}
            <i @click="onDelete(task.id)" style="color: red" class="fas fa-times">X</i>
             </h3>

    <p>Maintenance is due at {{task.day}}</p>
    </div>
</template>

<style>
.reminder {
    border:dashed 2px #41403E;
}
.task {
    color: rgb(15, 226, 103);

}

</style>


<script>

export default {
    name: "MyTask",
    props: {
        task: Object
    },
    methods: {
        onDelete(id) {
            this.$emit('delete-MyTask', id)
        }
    }
}

</script>
