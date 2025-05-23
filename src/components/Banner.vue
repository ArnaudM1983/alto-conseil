<template>
  <section class="relative overflow-hidden h-[30vh] md:h-screen sm:h-[80vh]">
    <!-- Desktop: background-image -->
    <div
      class="hidden md:block absolute inset-0 bg-center bg-cover parallax"
      :style="{ backgroundImage: `url('/terrasse2.png')` }"
    ></div>

    <!-- Mobile: img tag -->
    <img
      src="/terrasse2.png"
      alt="Terrasse"
      class="block md:hidden w-full h-full object-cover"
    />
  </section>
</template>

<style scoped>
.parallax {
  background-attachment: fixed;
  background-size: cover;
  background-repeat: no-repeat;
}
</style>
