<script setup>
import { ref } from 'vue'

const todos = ref([])
const newTodo = ref('')

const addTodo = () => {
  todos.value.push(newTodo.value)
  newTodo.value = ''
}

const removeTodo = (index) => {
  todos.value.splice(index, 1)
}
</script>

<template>
<input type="text" size="30" v-model="newTodo">
<button @click="addTodo()">追加</button>

<ul v-if="todos.length > 0">
  <li v-for="(todo, i) in todos" v-bind:key="i">{{ todo }} <span @click="removeTodo(i)" style="cursor: pointer">x</span></li>
</ul>
<p v-else>※ Todoを追加してください</p>
</template>