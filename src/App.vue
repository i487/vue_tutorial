<template>
  <div id="app">
    <div class="container">
      <Header title="Track" />
      <Tasks @delete-task= "deleteTask" :tasks="tasks" />
    </div>
    
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Tasks from './components/Tasks.vue'

export default {
  name: 'App',
  components: {
    Header,
    Tasks,
  },
  data () {
    return {
      tasks: []
    }
  },
  methods: {
    deleteTask (id) {
      console.log('task',id)
    }
  },
  created () {
    this.tasks = [
      {
        id: 1,
        text: "Kamila, my beloved ex-girlfriend",
        day: "she was born in 2000.01.01",
        reminder: true
      },
      {
        id: 2,
        text: "Jamila, my beloved ex-girlfriend",
        day: "she was born in 2001.01.10",
        reminder: true
      },
      {
        id: 3,
        text: "Kamola, my beloved ex-girlfriend",
        day: "she was born in 2004.10.01",
        reminder: true
      },
      {
        id: 4,
        text: "Dilnoza, my beloved current girlfriend",
        day: "she was born in 1998.09.05",
        reminder: false
      }
    ]
  }
  
}
</script>

<style lang="css">
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }

  .container {
    max-width: 1200px;
    padding: 0 15px;
    margin: 0 auto;
  }



</style>