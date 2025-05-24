<template>
    <div class="max-w-[1250px] mx-auto flex flex-wrap">
      <div
        v-for="(item, index) in items"
        :key="index"
        class="w-1/4 px-8"
        :class="index < 3 ? 'border-r border-gray-300' : ''"
      >
        <div>
          <!-- Ligne chiffre + icône -->
          <div class="flex items-center gap-4">
            <h2 class="text-4xl font-semibold text-gray-900">
              {{ item.number }}
            </h2>
  
            <div>
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
          </div>
  
          <!-- Texte sous le chiffre -->
          <div class="mt-4">
            <p class="text-left font-normal">
              {{ item.text }}
            </p>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script setup>
  const items = [
    {
      number: '10',
      text: 'Années d’expertise en transformation des PME et ETI.',
    },
    {
      number: '150',
      text: 'Projets menés avec méthode, impact et résultats concrets.',
    },
    {
      number: '95%',
      text: 'Clients satisfaits et fidèles à notre accompagnement humain.',
    },
    {
      number: '95%',
      text: 'Clients satisfaits et fidèles à notre accompagnement humain.',
    },
  ]
  </script>
  