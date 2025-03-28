<script setup lang="ts">
import { defineAsyncComponent, ref } from 'vue'
const AppButton = defineAsyncComponent(() => import('ui-app/AppButton'))
const count = ref(0)
</script>

<template>
  <!-- <button @click="count++"> {{ count }} </button> -->

  <Suspense>
    <template #default>
      <AppButton @click="count++"> {{ count }} </AppButton>
    </template>
    <template #fallback>
      <div>Loading remote component...</div>
    </template>
  </Suspense>
</template>
