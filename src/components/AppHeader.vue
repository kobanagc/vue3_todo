<script setup>
defineProps(['color'])
</script>
<template>
  <header>
    <h1 :style="{'color': color}"><slot>No title</slot></h1>
  </header>
</template>