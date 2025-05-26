<script setup>
import logo1 from '../assets/logo1.png'
import logo2 from '../assets/logo2.png'
import logo3 from '../assets/logo3.png'
import logo4 from '../assets/logo4.png'
import logo5 from '../assets/logo5.png'

const logos = [logo1, logo2, logo3, logo4, logo5]
</script>

<template>
    <section class="bg-gray-100 py-4 md:py-16">
      <div class=" mx-auto overflow-hidden">
        <div class="flex animate-scroll gap-25 items-center">  <!-- gap-8 ici -->
          <!-- Logos originaux -->
          <div
            v-for="(logo, index) in logos"
            :key="index"
            class="flex-shrink-0"
          >
            <img :src="logo" alt="logo" class="h-32 object-contain" />
          </div>
  
          <!-- Logos dupliqués -->
          <div
            v-for="(logo, index) in logos"
            :key="'duplicate-' + index"
            class="flex-shrink-0"
          >
            <img :src="logo" alt="logo" class="h-32 object-contain" />
          </div>
        </div>
      </div>
    </section>
  </template>
  

<style scoped>
@keyframes scroll {
  0% {
    transform: translateX(0%);
  }
  100% {
    transform: translateX(-50%);
  }
}

.animate-scroll {
  animation: scroll 15s linear infinite;
}
</style>
