<template>
    <div ref="container" :class="{ 'fade-in-up': isVisible }">
      <slot />
    </div>
  </template>
  
  <script setup>
  import { ref, onMounted, onUnmounted } from 'vue'
  
  const container = ref(null)
  const isVisible = ref(false)
  
  onMounted(() => {
    const observer = new IntersectionObserver(([entry]) => {
      if (entry.isIntersecting) {
        isVisible.value = true
        observer.disconnect()
      }
    }, { threshold: 0.1 })
  
    if (container.value) observer.observe(container.value)
  
    onUnmounted(() => observer.disconnect())
  })
  </script>
  
  <style scoped>
  @keyframes myAnim {
    0% {
      opacity: 0;
      transform: translateY(50px);
    }
    100% {
      opacity: 1;
      transform: translateY(0);
    }
  }
  
  .fade-in-up {
    animation: myAnim 2s ease 0s 1 normal forwards;
  }
  </style>
  