<script setup lang="ts"></script>

<template>
  <button class="btn-neon">
    Я тоже отдельный микрофронт
    <slot />
  </button>
</template>

<style scoped>
.btn-neon {
  padding: 12px 28px;
  background: transparent;
  border: 2px solid #0ef;
  border-radius: 8px;
  color: #0ef;
  font-weight: 600;
  font-size: 16px;
  text-transform: uppercase;
  cursor: pointer;
  position: relative;
  overflow: hidden;
  transition: all 0.3s ease;
  box-shadow: 0 0 10px rgba(0, 238, 255, 0.3);
}

.btn-neon:hover {
  background: #0ef;
  color: #111;
  box-shadow: 0 0 20px rgba(0, 238, 255, 0.6);
  transform: translateY(-2px);
}

.btn-neon::before {
  content: '';
  position: absolute;
  top: 0;
  left: -100%;
  width: 100%;
  height: 100%;
  background: linear-gradient(90deg, transparent, rgba(0, 238, 255, 0.4), transparent);
  transition: 0.5s;
}

.btn-neon:hover::before {
  left: 100%;
}
</style>
