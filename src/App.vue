<template>
  <div id="app">
    <h2>Todo Application</h2>
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <Todo/>
  </div>
</template>

<script>
import Todo from './components/Todo.vue'

export default {
  name: 'App',
  components: {
    Todo
  }
}
</script>

<style>
#app {
  position: fixed;
  top: 20%;
  left: 50%;
  margin-top: -50px;
  margin-left: -100px;

}
h2 {
  position: fixed;
  top: 0%;
  left: 50%;
  margin-top: -50px;
  margin-left: -100px;
  color: blueviolet;
  font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
}
</style>
