<script setup lang="ts">
import AppCounter from './components/AppCounter.vue'
</script>

<template>
  <div class="remote-app">
    <h2>Микрофронт</h2>
    <AppCounter />
  </div>
</template>

<style scoped>
.remote-app {
  border: 2px dashed #ccc;
  padding: 20px;
  margin: 20px 0;
}
</style>
