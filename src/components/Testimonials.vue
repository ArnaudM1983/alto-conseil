<script setup>
import testimonialsImg from '@/assets/testimonial.png'
</script>

<template>
  <section class="">
    <div class="container px-6 py-10 mx-auto">
      <div class="lg:flex lg:items-center lg:space-x-10">
        <div class="lg:w-1/3">
          <img
            class="object-cover object-center w-48 h-48 mx-auto rounded-full"
            :src="testimonialsImg"
            alt="testimonial image"
          />
        </div>

        <div class="mt-8 lg:mt-0 lg:w-2/3">
          <span class="text-gray-500 block text-left text-7xl font-semibold">“</span>

          <h4 class="text-left font-semibold">
            Ce que disent nos clients à propos de nos services
          </h4>

          <h5 class="text-left mt-6">
            Nous avons sollicité ce cabinet dans une période charnière pour notre entreprise. Leur capacité
            à structurer les enjeux, proposer une vision claire et surtout actionnable a été déterminante.
            Leur approche est à la fois rigoureuse, humaine et orientée résultats. Nous continuons à
            collaborer sur plusieurs axes.
          </h5>

          <h3 class="text-left mt-6">Claire Dumont</h3>
          <p class="text-left">
            NovaTerra Industries
          </p>

          <div class="flex items-center justify-between mt-12 lg:justify-start">
            <button
              title="left arrow"
              class="p-2 border rounded-full transition-colors duration-300 text-[#fe5b2c] border-[#fe5b2c] hover:bg-[#fe5b2c] hover:text-white dark:hover:bg-[#fe5b2c]"
            >
              <svg xmlns="http://www.w3.org/2000/svg" class="w-6 h-6" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                <path stroke-linecap="round" stroke-linejoin="round" d="M15 19l-7-7 7-7" />
              </svg>
            </button>

            <button
              title="right arrow"
              class="p-2 border rounded-full transition-colors duration-300 text-[#fe5b2c] border-[#fe5b2c] lg:mx-6 hover:bg-[#fe5b2c] hover:text-white dark:hover:bg-[#fe5b2c]"
            >
              <svg xmlns="http://www.w3.org/2000/svg" class="w-6 h-6" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                <path stroke-linecap="round" stroke-linejoin="round" d="M9 5l7 7-7 7" />
              </svg>
            </button>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
