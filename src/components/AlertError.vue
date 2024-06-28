<template>
  <div class="alert-error" v-if="show">
    <span class="alert-content">
      <svg xmlns="http://www.w3.org/2000/svg" width="1.5rem" height="1.5rem" viewBox="0 0 24 24" fill="none"
        stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
        <circle cx="12" cy="12" r="10"></circle>
        <line x1="12" y1="8" x2="12" y2="12"></line>
        <line x1="12" y1="16" x2="12.01" y2="16"></line>
      </svg>
      {{ message }}
    </span>
    <div class="progress-bar">
    </div>
  </div>
</template>

<script setup lang="ts">
defineProps<{
  show: boolean;
  message: string;
}>();
</script>

<style scoped>
.alert-error {
  background-color: #fef2f2;
  border: 1px solid #fee2e2;
  border-radius: 4px;
  color: #991b1b;
  padding: 0.75rem 1rem;
  margin-bottom: 1rem;
  position: relative;
  overflow: hidden;
}

.alert-content {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 0.5rem;
  font-weight: 600;
  font-size: 1.5rem;
}

svg {
  color: #991b1b;
}

.progress-bar {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 10px;
  background-color: #991b1b;
  animation: shrink 3s linear forwards;
}

@keyframes shrink {
  from {
    width: 100%;
  }
  100% {
    width: 0;
  }
}
</style>