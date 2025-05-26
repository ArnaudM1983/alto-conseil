<template>
  <header class="absolute top-0 left-0 right-0 z-50 bg-transparent text-white max-w-[1300px] mx-auto">


    <div class="flex justify-between items-center p-6">

      <!-- Mobile Toggle Button -->
      <div class="md:hidden fixed top-4 left-1/2 transform -translate-x-1/2 z-50">
        <button @click="isMenuOpen = !isMenuOpen"
          class="w-14 h-14 flex items-center justify-center rounded-full bg-black/10 backdrop-blur-md text-black text-4xl shadow-lg">
          <Icon :icon="isMenuOpen ? 'material-symbols:close' : 'material-symbols:menu'" />
        </button>
      </div>

      <!-- Logo -->
      <div> <img :src="AltoLogo" alt="Alto Logo" class="h-10 md:h-24 object-contain" /></div>

      <!-- Nav Links -->
      <nav :class="[
        'left-1/2 w-[280px] p-6 flex flex-col items-center gap-6 shadow-md md:flex-row md:gap-16 md:p-0',
        isMenuOpen ? 'flex fixed top-[90px] -translate-x-1/2 bg-black/20 backdrop-blur-md rounded-lg' : 'hidden',
        'md:static md:w-auto md:bg-transparent md:backdrop-blur-0 md:shadow-none md:flex md:translate-x-0 md:left-auto md:max-w-full md:rounded-none'
      ]">

        <a href="#" @click.prevent="scrollToSection('#')"
          class="relative text-white font-light text-xl after:content-[''] after:absolute after:left-0 after:-bottom-1 after:w-0 after:h-[1px] after:bg-white after:transition-all after:duration-300 hover:after:w-full">Accueil</a>
        <a href="#apropos" @click.prevent="scrollToSection('#apropos')"
          class="relative text-white font-light text-xl after:content-[''] after:absolute after:left-0 after:-bottom-1 after:w-0 after:h-[1px] after:bg-white after:transition-all after:duration-300 hover:after:w-full">A
          propos</a>
        <a href="#expertises" @click.prevent="scrollToSection('#expertises')"
          class="relative text-white font-light text-xl after:content-[''] after:absolute after:left-0 after:-bottom-1 after:w-0 after:h-[1px] after:bg-white after:transition-all after:duration-300 hover:after:w-full">Nos
          expertises</a>
        <a href="#contact" @click.prevent="scrollToSection('#contact')"
          class="relative text-white font-light text-xl after:content-[''] after:absolute after:left-0 after:-bottom-1 after:w-0 after:h-[1px] after:bg-white after:transition-all after:duration-300 hover:after:w-full">Contact</a>
      </nav>

      <!-- Réserver Button -->
      <!-- <a href="#contact"
        class="hidden md:inline-block text-black border border-black px-6 py-2 text-lg font-light cursor-pointer bg-transparent rounded-none hover:bg-white hover:text-black transition">
        Je réserve
      </a> -->

    </div>
  </header>
</template>

<script setup>
import { ref } from 'vue'
import { Icon } from '@iconify/vue'

import AltoLogo from '@/assets/alto-logo.png'

const isMenuOpen = ref(false)

const scrollToSection = (id) => {
  isMenuOpen.value = false
  const section = document.querySelector(id)
  if (section) section.scrollIntoView({ behavior: 'smooth' })
}
</script>