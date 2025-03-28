<script setup lang="ts">
import { defineAsyncComponent } from 'vue'

const RemoteVueApp = defineAsyncComponent(() => import('remote-app/App'))
</script>

<template>
  <div>
    <h1>Хост приложение</h1>
    <RemoteVueApp />
  </div>
</template>
