<template>
  <header class="absolute top-0 left-0 w-full z-50 bg-transparent text-white">

    <div class="flex justify-between items-center p-6 lg:px-12">

      <!-- Mobile Toggle Button -->
      <div class="md:hidden fixed top-4 left-1/2 transform -translate-x-1/2 z-50">
        <button @click="isMenuOpen = !isMenuOpen"
          class="w-14 h-14 flex items-center justify-center rounded-full bg-black/10 backdrop-blur-md text-black text-4xl shadow-lg">
          <Icon :icon="isMenuOpen ? 'material-symbols:close' : 'material-symbols:menu'" />
        </button>
      </div>


      <!-- Nav Links -->
      <nav :class="[
        'left-1/2 w-[280px] p-6 flex flex-col items-center gap-6 shadow-md md:flex-row md:gap-16 md:p-0',
        isMenuOpen ? 'flex fixed top-[90px] -translate-x-1/2 bg-black/20 backdrop-blur-md rounded-lg' : 'hidden',
        'md:static md:w-auto md:bg-transparent md:backdrop-blur-0 md:shadow-none md:flex md:translate-x-0 md:left-auto md:max-w-full md:rounded-none'
      ]">




        <a href="#lappartement" @click.prevent="scrollToSection('#lappartement')"
          class="relative text-black font-light uppercase text-xl after:content-[''] after:absolute after:left-0 after:-bottom-1 after:w-0 after:h-[1px] after:bg-black after:transition-all after:duration-300 hover:after:w-full">L'Appartement</a>
        <a href="#equipements" @click.prevent="scrollToSection('#equipements')"
          class="relative text-black font-light uppercase text-xl after:content-[''] after:absolute after:left-0 after:-bottom-1 after:w-0 after:h-[1px] after:bg-black after:transition-all after:duration-300 hover:after:w-full">Equipements</a>
        <a href="#faq" @click.prevent="scrollToSection('#faq')"
          class="relative text-black font-light uppercase text-xl after:content-[''] after:absolute after:left-0 after:-bottom-1 after:w-0 after:h-[1px] after:bg-black after:transition-all after:duration-300 hover:after:w-full">FAQ</a>
      </nav>

      <!-- Logo -->
      <!-- <div class="text-3xl text-red-500 font-bold">LOGO</div> -->

      <!-- Réserver Button -->
      <a href="#contact"
        class="hidden md:inline-block text-black border border-black px-6 py-2 text-lg font-light cursor-pointer bg-transparent rounded-none hover:bg-white hover:text-black transition">
        Je réserve
      </a>

    </div>
  </header>
</template>

<script setup>
import { ref } from 'vue'
import { Icon } from '@iconify/vue'

const isMenuOpen = ref(false)

const scrollToSection = (id) => {
  isMenuOpen.value = false
  const section = document.querySelector(id)
  if (section) section.scrollIntoView({ behavior: 'smooth' })
}
</script>