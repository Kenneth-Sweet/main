<template>
  <div class="home">
    <div class="container"><img alt="Vue logo" src="../assets/astraheader1.png">
    <MyHeader></MyHeader>
    </div>
    
  </div>
</template>



<script>
// @ is an alias to /src
import MyHeader from '../components/MyHeader'

export default {
  name: 'App',
  components: {
    MyHeader,
  },
  
}
</script>
