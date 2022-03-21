<template>
    <button @click="onClick()" class="btn raise">{{text}}</button>
</template>


<script>
    export default {
        name: 'SimpleButton',
        props: {
            text: String,
            color: String,
        },
    methods: {
        onClick() {
            console.log('click')
        }
    }
}
</script>