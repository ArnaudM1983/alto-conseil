<script setup>
import bloc1 from '@/assets/bloc1.png'
</script>

<template>

  <!-- Image à droite et Texte à gauche sur desktop -->
  <section id="apropos">
    <div class="mx-auto max-w-[1250px] px-4 py-8 sm:px-6 lg:px-0">
      <div class="grid grid-cols-1 gap-4 md:grid-cols-2 md:items-center md:gap-24">
        <div class="order-2 md:order-1">
          <div class="max-w-lg md:max-w-none text-left">
            <h4 class="mb-5">Une équipe experte, engagée à vos côtés</h4>
            <h2 class=" font-semibold text-white sm:text-3xl">
              Une expertise dédiée à votre réussite
            </h2>
            <p class="mt-4">
              Depuis plus de 10 ans, Alto Conseil accompagne les PME et ETI dans leurs enjeux de transformation. Notre
              approche est pragmatique, humaine et orientée résultats. Notre mission : vous permettre de gagner en
              clarté, efficacité et impact.
            </p>
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1" stroke-linecap="round"
              stroke-linejoin="round" xmlns="http://www.w3.org/2000/svg" aria-hidden="true" class="mb-2 w-20 h-20">
              <line x1="7" y1="17" x2="17" y2="7"></line>
              <polyline points="7 7 17 7 17 17"></polyline>
            </svg>
            <a href="#contact"
              class="inline-block bg-[#fe5b2c] text-white px-8 py-4 font-dm text-lg leading-6 transition duration-200 hover:bg-[#e14e26] hover:text-white">
              Contactez-nous
            </a>
          </div>
        </div>
        <div class="order-1 md:order-2">
          <img :src="bloc1" class="" alt="Equipe" />
        </div>
      </div>
    </div>
  </section>

</template>
