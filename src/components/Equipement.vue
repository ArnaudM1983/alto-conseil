<template>
    <section class="max-w-[1250px] mx-auto py-8 px-4 md:px-0" id="equipements">
      <h2 class="text-3xl mb-8 md:text-6xl font-semibold text-white sm:text-3xl text-left">
        Aperçu de l’appartement
      </h2>
      
      <!-- Première grille : pièces -->
      <div class="grid grid-cols-1 md:grid-cols-3 gap-4 text-white px-0 md:px-0">
        <div v-for="(item, index) in pieces" :key="'piece-' + index"
          class="flex justify-between items-center border-b border-white py-4">
          <span class="text-lg">{{ item.name }}</span>
          <span class="text-lg font-semibold">{{ item.value }}</span>
        </div>
      </div>
  
      <h2 class="text-2xl mt-12 md:text-5xl font-semibold text-white sm:text-3xl text-left">
        Equipements
      </h2>
      <!-- Deuxième grille : équipements -->
      <div class="grid grid-cols-1 md:grid-cols-3 gap-4 text-white mt-4 px-0 md:px-0">
        <div v-for="(item, index) in equipements" :key="'equipement-' + index"
          class="flex justify-between items-center border-b border-white py-4">
          <span class="text-lg">{{ item.name }}</span>
          <span class="text-lg font-semibold" v-if="item.value">{{ item.value }}</span>
        </div>
      </div>
    </section>
  </template>
  
  <script setup>
  const pieces = [
    { name: 'Chambres', value: 2 },
    { name: 'Salle de bain', value: 1 },
    { name: 'Cuisine', value: 1 },
    { name: 'Salon', value: 1 },
    { name: 'Terrasse', value: 1 },
    { name: 'Place de parking', value: 1 },
    { name: 'Bureau', value: 1 },
    { name: 'Toilettes', value: 2 },
    { name: 'Buanderie', value: 1 },
  ]
  
  const equipements = [
    { name: 'Climatisation' },
    { name: 'Chauffage' },
    { name: 'Lave-linge' },
    { name: 'Lave-vaisselle' },
    { name: 'Wi-Fi' },
    { name: 'TV Ecran Plat' },
  ]
  </script>
  