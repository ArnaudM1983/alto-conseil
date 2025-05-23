<template>
  <div class="overflow-hidden w-full mx-auto pt-12">
    <div class="flex animate-scroll gap-0">
      <div
        v-for="(img, index) in images"
        :key="index"
        class="flex-shrink-0 square-img"
      >
        <img :src="img" alt="bannière image" class="w-full h-full object-cover" />
      </div>

      <div
        v-for="(img, index) in images"
        :key="'duplicate-' + index"
        class="flex-shrink-0 square-img"
      >
        <img :src="img" alt="bannière image" class="w-full h-full object-cover" />
      </div>
    </div>
  </div>
</template>

<script setup>
import carre1 from '@/assets/carre1.png'
import carre2 from '@/assets/carre2.png'
import carre3 from '@/assets/carre3.png'
import carre4 from '@/assets/carre4.png'

const images = [carre1, carre2, carre3, carre4]
</script>

<style scoped>
.square-img {
  aspect-ratio: 1 / 1;
  min-height: 200px;
  flex-basis: 50%; 
}

@media (min-width: 768px) {
  .square-img {
    flex-basis: 25%; 
    min-height: auto; 
  }
}

@keyframes scroll {
  0% {
    transform: translateX(0%);
  }
  100% {
    transform: translateX(-50%);
  }
}

.animate-scroll {
  animation: scroll 10s ease-in-out infinite alternate;
}
</style>
