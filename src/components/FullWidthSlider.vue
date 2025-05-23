<template>
  <div class="relative overflow-hidden">
    <div class="wrapper" ref="wrapper">
      <section v-for="(slide, i) in slides" :key="i" class="panel relative">
        <div class="w-full h-full p-4 md:p-10 relative">
          <img :src="slide.image" class="w-full h-auto min-h-[400px] md:h-full md:max-h-none object-cover shadow-lg"
          /> />
          <!-- Overlay gradient -->
          <div class="absolute bottom-0 left-0 w-full h-[40%] bg-gradient-to-t from-neutral-900 to-transparent z-10"></div>
          <!-- Text bottom left -->
          <div class="absolute left-24 bottom-24 text-white text-xl md:text-4xl font-light lora-font z-20">
            {{ slide.leftText }}
          </div>
          <!-- Text bottom right -->
          <div class="absolute bottom-24 right-24 text-white text-xl md:text-3xl font-light z-20">
            {{ slide.rightText }}
          </div>
        </div>
      </section>
    </div>
  </div>
</template>

<script setup>
import { onMounted, ref, nextTick } from 'vue'
import { gsap } from 'gsap'
import { ScrollTrigger } from 'gsap/ScrollTrigger'

import plage from '../assets/chambre.png'
import cuisine from '../assets/cuisine.png'
import terrasse2 from '../assets/terrasse2.png'

gsap.registerPlugin(ScrollTrigger)

const wrapper = ref(null)
const slides = [
  { image: plage, leftText: 'Chambre Principale', rightText: '15m2' },
  { image: cuisine, leftText: 'Cuisine', rightText: '' },
  { image: terrasse2, leftText: 'Terrasse', rightText: '20m2' },
]

onMounted(async () => {
  await nextTick()

  // Activation GSAP horizontal scroll uniquement sur desktop (min-width: 768px)
  gsap.matchMedia().add("(min-width: 768px)", () => {
    const sections = wrapper.value.querySelectorAll('.panel')

    return gsap.to(sections, {
      xPercent: -100 * (sections.length - 1),
      ease: 'none',
      scrollTrigger: {
        trigger: wrapper.value,
        pin: true,
        scrub: 0.5,
        snap: 1 / (sections.length - 1),
        start: 'top top',
        end: () => "+=" + wrapper.value.offsetWidth,
      },
    })
  })
})
</script>

<style scoped>

/* Masquer le texte sur mobile */
.panel > div > .absolute {
  display: none;
}

/* Afficher sur desktop */
@media (min-width: 768px) {
  .panel > div > .absolute {
    display: block;
  }
}

.wrapper {
  display: flex;
  flex-direction: column; /* vertical empilement par défaut */
  height: auto;
}

.panel {
  width: 100%;
  height: auto;
  position: relative;
}

.lora-font {
  font-family: 'Lora', serif;
}

@media (min-width: 768px) {
  .wrapper {
    flex-direction: row; /* horizontal sur desktop */
    width: 300vw; /* 3 sections * 100vw */
    height: 100vh; /* plein écran */
  }
  .panel {
    flex: 0 0 100vw;
    height: 100vh;
  }
}
</style>
