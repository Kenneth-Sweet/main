<template>
  <div class='container' style="color: #eee">
        <h1>{{title}}</h1>

  </div>

</template>

<script>


export default {
    name: 'MyHeader',
    props: 
        {
        title: {
        type: String,
        default: 'Default'
      },
    }
}
</script>

<style>

</style>