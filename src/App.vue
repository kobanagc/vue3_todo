<script setup>
import { ref } from 'vue'

const todos = ref([])
const newTodo = ref('')

const addTodo = () => {
  todos.value.push(newTodo.value)
  newTodo.value = ''
}
</script>

<template>
<input type="text" size="30" v-model="newTodo">
<button @click="addTodo()">追加</button>

<ul>
  <li v-for="(todo, i) in todos" v-bind:key="i">{{i}}.{{ todo }}</li>
</ul>
</template>