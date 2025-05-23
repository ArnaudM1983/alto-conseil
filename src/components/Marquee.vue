<template>
    <section
      class=" md:mt-36 overflow-hidden whitespace-nowrap bg-neutral-300 text-black py-6 md:py-12 border-t border-b border-gray-500"
    >
      <div
        ref="marquee"
        class="inline-block"
        :style="{ transform: `translateX(${offset}px)` }"
      >
        <span class="mx-10 text-3xl md:text-6xl font-light">TEXTE</span>
        <span class="mx-10 text-3xl md:text-6xl">TEXTE</span>
        <span class="mx-10 text-3xl md:text-6xl">TEXTE</span>
        <span class="mx-10 text-3xl md:text-6xl font-light">TEXTE</span>
        <span class="mx-10 text-3xl md:text-6xl">TEXTE</span>
        <span class="mx-10 text-3xl md:text-6xl">TEXTE</span>
        <span class="mx-10 text-3xl md:text-6xl font-light">TEXTE</span>
        <span class="mx-10 text-3xl md:text-6xl">TEXTE</span>
        <span class="mx-10 text-3xl md:text-6xl">TEXTE</span>
      </div>
    </section>
  </template>
  
  <script setup>
import { ref, onMounted, onUnmounted } from "vue";

const offset = ref(0);         // Position visible (affichée)
const targetOffset = ref(0);   // Destination basée sur scroll
const marquee = ref(null);

let lastScrollY = 0;
let animationFrameId;

const handleScroll = () => {
  const currentY = window.scrollY;
  const delta = currentY - lastScrollY;

  targetOffset.value -= delta * 0.5; // sensibilité 
  lastScrollY = currentY;
};

const animate = () => {
  offset.value += (targetOffset.value - offset.value) * 0.1; 
  animationFrameId = requestAnimationFrame(animate);
};

onMounted(() => {
  lastScrollY = window.scrollY;   // initialise la position réelle du scroll
  handleScroll();                 // déclenche une première mise à jour immédiate
  window.addEventListener("scroll", handleScroll);
  animate();
});

onUnmounted(() => {
  window.removeEventListener("scroll", handleScroll);
  cancelAnimationFrame(animationFrameId);
});
</script>


  
  <style scoped>
  span {
    font-family: "urbanist", sans-serif;
    font-weight: 100;
  }
  
  /* Pour lisser le mouvement */
  section {
    will-change: transform;
  }
  </style>
  