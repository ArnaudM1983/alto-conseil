<template>
  <div
    ref="statsSection"
    class="max-w-[1250px] mx-auto flex flex-wrap"
  >
    <div
      v-for="(item, index) in items"
      :key="index"
      class="w-full md:w-1/4 px-8"
      :class="index < items.length - 1 ? 'border-r border-gray-300' : ''"
    >
      <div>
        <!-- Ligne chiffre + icône -->
        <div class="flex items-center gap-4">
          <h2 class="text-4xl font-semibold text-gray-900">
            {{ displayNumbers[index] }}
          </h2>

          <svg
            viewBox="0 0 24 24"
            fill="none"
            stroke="currentColor"
            stroke-width="1"
            stroke-linecap="round"
            stroke-linejoin="round"
            xmlns="http://www.w3.org/2000/svg"
            aria-hidden="true"
            class="w-16 h-16"
          >
            <line x1="7" y1="17" x2="17" y2="7"></line>
            <polyline points="7 7 17 7 17 17"></polyline>
          </svg>
        </div>

        <!-- Texte sous le chiffre -->
        <div class="mt-4">
          <p class="text-left font-normal">{{ item.text }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref, onMounted } from 'vue'

const statsSection = ref(null)
const hasAnimated = ref(false)

const items = [
  { number: 10, text: 'Années d’expertise en transformation des PME et ETI.' },
  { number: 150, text: 'Projets menés avec méthode, impact et résultats concrets.' },
  { number: 95, text: '% Clients satisfaits et fidèles à notre accompagnement humain.' },
  { number: 95, text: '% Clients satisfaits et fidèles à notre accompagnement humain.' },
]

const displayNumbers = ref(items.map(() => 0))

const animateCountUp = (index, target, duration = 2000) => {
  const startTime = performance.now()

  const step = (now) => {
    const progress = Math.min((now - startTime) / duration, 1)
    displayNumbers.value[index] = Math.floor(progress * target)
    if (progress < 1) requestAnimationFrame(step)
  }

  requestAnimationFrame(step)
}

const startAnimation = () => {
  if (hasAnimated.value) return
  hasAnimated.value = true
  items.forEach((item, index) => {
    animateCountUp(index, item.number)
  })
}

onMounted(() => {
  const observer = new IntersectionObserver(
    (entries) => {
      if (entries[0].isIntersecting) {
        startAnimation()
        observer.disconnect()
      }
    },
    { threshold: 0.3 } // Déclenche quand 30% est visible
  )

  if (statsSection.value) {
    observer.observe(statsSection.value)
  }
})
</script>
