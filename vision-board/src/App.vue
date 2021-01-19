<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <h1>2021 Vision Board</h1>
    <Goals v-bind:goals="goals"/>
    <AddGoal v-on:add-goal="addGoal" />
  
  </div>
</template>

<script>
import Goals from './components/Goals';
import AddGoal from './components/AddGoal';

export default {
  name: 'App',
  components: {
    Goals,
    AddGoal
  },
  data(){
    return {
      goals: [
        {
          id: 1,
          title: "Secure new software engineering role",
          completed: false
        },
        {
          id: 2,
          title: "Move to a coastal city",
          completed: false
        },
        {
          id: 3,
          title: "Monetize one YouTube channel",
          completed: true
        }
      ]
    }
  },
  addGoal(newGoal){
    this.goals = [...this.goals, newGoal];
  }
}
</script>

<style>
* {
  box-sizing: border-box;
  margin:0;
  padding:0;
}

body {
  font-family: Arial, Helvetica, sans-serif;
  line-height: 1.4;
  background-color: #061639;
  color: #fff;
  text-align: center;
}

.btn {
  display: inline-block;
  border: none;
  background: #555;
  color: #fff;
  padding: 7px 20px;
  cursor: pointer;
}

.btn:hover {
  background: #666;
}
</style>
