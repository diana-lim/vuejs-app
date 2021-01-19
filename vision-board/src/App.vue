<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <h1>2021 Vision Board</h1>
    <Goals v-bind:goals="goals" />
  
  </div>
</template>

<script>
import Goals from './components/Goals';

export default {
  name: 'App',
  components: {
    Goals
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
          completed: false
        }
      ]
    }
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
</style>
