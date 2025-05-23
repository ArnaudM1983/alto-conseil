<template>
    <section class="relative overflow-hidden max-w-[1250px] mx-auto">
      <h2 class="text-3xl mb-8 md:text-6xl font-semibold text-white sm:text-3xl text-left px-4 sm:px-6">
        Emplacement Idéal
      </h2>
  
      <div class="relative h-[80vh] w-full overflow-hidden">
        <img
          :src="map"
          alt="Slide image"
          class="object-cover w-full h-full transition-opacity duration-500"
        />
  
        <!-- Overlay -->
        <div class="absolute inset-0 bg-gradient-to-t from-neutral-900 to-transparent"></div>
      </div>
  
      <!-- Texte positionné à gauche -->
      <div class="flex justify-start mt-16 text-left px-4 sm:px-6">
        <div class="w-full md:w-1/2 pr-4 text-white">
            <p class="text-xl md:text-2xl leading-relaxed">
            Le Rayol-Canadel-sur-Mer offre un cadre naturel exceptionnel entre mer et collines méditerranéennes. Découvrez ses plages préservées, les îles de Porquerolles et Port-Cros à proximité, ainsi que de nombreux sentiers de randonnée pour explorer ce coin de paradis.
          </p>
        </div>
      </div>
    </section>
  </template>
  
  <script setup>
  import map from '@/assets/map.png'
  </script>
  