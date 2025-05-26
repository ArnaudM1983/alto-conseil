<template>
  <section class="relative overflow-hidden h-[100vh] md:h-screen flex items-center">
    <!-- Conteneur central -->
    <div class="relative z-10 flex flex-col justify-center w-full max-w-[1250px] mx-auto px-4 md:px-8 md:flex-row">
      <!-- Colonne vide à gauche (desktop uniquement) -->
      <div class="hidden md:block w-1/2"></div>

      <!-- Colonne droite avec 3 paragraphes -->
      <div class="w-full md:w-1/2 p-8 text-white text-left space-y-6">
        <p>Une stratégie globale pour relever les défis de demain.</p>
        <h2>Engagés à fournir des conseils précis et exploitables pour accompagner vos décisions financières avec confiance.</h2>
        <p>Vision stratégique. Partenaire de confiance.</p>
      </div>
    </div>

    <!-- Desktop: background-image -->
    <div
      class="hidden md:block absolute inset-0 bg-center bg-cover parallax"
      :style="{ backgroundImage: `url('/banner.png')` }"
    ></div>

    <!-- Mobile: img tag (plein écran et responsive) -->
    <img
      src="/banner.png"
      alt="Terrasse"
      class="block md:hidden absolute inset-0 w-full h-full object-cover"
    />

    <!-- Overlay radial (adapté à toutes tailles) -->
    <div
      class="absolute inset-0 z-0 pointer-events-none"
      :style="{
        background: 'radial-gradient(circle at center, rgba(232,79,36,0.9) 0%, rgba(34,34,34,0.5) 51%, transparent 90%)'
      }"
      aria-hidden="true"
    ></div>
  </section>
</template>

<style scoped>
.parallax {
  background-attachment: fixed;
  background-size: cover;
  background-repeat: no-repeat;
}

p {
  color: white !important;
}

h2 {
  color: white !important;
}
</style>
