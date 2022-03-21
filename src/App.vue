<template>
  <div class="home">
    <div class="container"><img alt="Vue logo" src="./assets/astraheader1.png">
    <MyHeader title="Ship Tracker"></MyHeader>
    <SimpleButton color="green" text="Add Ship" ></SimpleButton>
    <SimpleButton color="red" text="Delete Ship" ></SimpleButton>
    <SimpleButton color="Blue" text="Update Ship" ></SimpleButton>
    <MyTasks @deleteMyTask="deleteMyTask" :tasks="tasks"></MyTasks>
    </div>
    
  </div>
</template>

<script>
// @ is an alias to /src
import MyHeader from './components/MyHeader'
import SimpleButton from './components/SimpleButton.vue'
import MyTasks from './components/tasks.vue'

export default {
  name: 'App',
  components: {
    MyHeader,
    SimpleButton,
    MyTasks
  },
  data() {
    return {
      task: []
    }
  },
  methods: {
    deleteMyTask(id){
      console.log(this.tasks)
      if(confirm('Are you sure?')){
      this.tasks = this.tasks.filter((tasks) => tasks.id !== id)
      }
      
    },
  },

  created() {
    this.tasks = [{
      id: 1,
      text: 'Carrier Class',
      day: 'March 1st at 2:30pm',
      reminder: true
      },
      {
      id: 2,
      text: 'Sprinter Class',
      day: 'March 2st at 2:30pm',
      reminder: false
      },
      {
        id: 3,
      text: 'Sprinter Class',
      day: 'March 2st at 2:30pm',
      reminder: false
      }
    
    ]
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}

.btn{
    background: none;
  border: 2px solid;
  font: inherit;
  line-height: 1;
  margin: 0.5em;
  padding: 1em 2em;
  color: #eee
}
body{
  color: #fff;
  background: hsl(227, 10%, 10%);
  font: 300 1em 'Fira Sans', sans-serif;
  
  justify-content: center;
  align-content: center;
  align-items: center;
  text-align: center;
  
  display: flex;
}
.raise:hover,
.raise:focus {
  box-shadow: 0 0.5em 0.5em -0.4em #ffa260;
  transform: translateY(-0.25em);
}

</style>
