<script setup>
import { computed,ref } from 'vue'

const message = computed(() => {
  return 'ようこそ<strong>' + myName.value + '</strong>さん'
})
const welcomeColor = 'red'
const myName = ref('')
</script>

<template>
<h1>Vue 3</h1>
<p>お名前は？：<input type="text" size="30" v-model="myName"></p>
<p v-html="message" v-bind:style="{color: welcomeColor}"></p>
</template>

