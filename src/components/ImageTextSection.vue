<script setup>
import plage from '@/assets/plage.png'
import deco from '@/assets/deco.png'
import plage2 from '@/assets/plage2.png'
</script>

<template>
  <!-- Image à gauche et Texte à droite sur desktop -->
  <section>
    <div class="mx-auto max-w-[1250px] px-4 py-8 sm:px-6 lg:px-0">
      <div class="grid grid-cols-1 gap-4 md:grid-cols-2 md:items-center md:gap-24">
        <div class="md:order-1">
          <img :src="plage" class="" alt="Plage" />
        </div>
        <div class="md:order-2">
          <div class="max-w-lg md:max-w-none text-left">
            <h2 class="text-3xl md:text-6xl font-semibold text-white sm:text-3xl">
              Emplacement Idéal
            </h2>
            <p class="mt-4">
              Situé dans un quartier paisible du Rayol-Canadel-sur-Mer, l’appartement offre un accès rapide aux commodités locales. En moins de 5 minutes, vous rejoignez les commerces de proximité, et en 10 minutes à pied, la plage du Canadel vous accueille pour des journées ensoleillées au bord de l’eau.
            </p>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Image à droite et Texte à gauche sur desktop -->
  <section>
  <div class="mx-auto max-w-[1250px] px-4 py-8 sm:px-6 lg:px-0">
    <div class="grid grid-cols-1 gap-4 md:grid-cols-2 md:items-center md:gap-24">
      <div class="order-2 md:order-1">
        <div class="max-w-lg md:max-w-none text-left">
          <h2 class="text-3xl md:text-6xl font-semibold text-white sm:text-3xl">
            Confort pratique
          </h2>
          <p class="mt-4">
            Pensé pour les séjours en couple ou en famille, l’appartement dispose d’une chambre indépendante, d’un séjour lumineux avec canapé convertible, et d’une cuisine entièrement équipée. Tout a été conçu pour que vous vous sentiez comme chez vous, avec confort et simplicité.
          </p>
        </div>
      </div>
      <div class="order-1 md:order-2">
        <img :src="deco" class="" alt="Décoration" />
      </div>
    </div>
  </div>
</section>


  <!-- Image à gauche et Texte à droite sur desktop -->
  <section>
    <div class="mx-auto max-w-[1250px] px-4 py-8 sm:px-6 lg:px-0">
      <div class="grid grid-cols-1 gap-4 md:grid-cols-2 md:items-center md:gap-24">
        <div class="md:order-1">
          <img :src="plage2" class="" alt="Plage 2" />
        </div>
        <div class="md:order-2">
          <div class="max-w-lg md:max-w-none text-left">
            <h2 class="text-3xl md:text-6xl font-semibold text-white sm:text-3xl">
              Région magique
            </h2>
            <p class="mt-4">
              Explorez les merveilles naturelles du Rayol et ses alentours : balades dans le Domaine du Rayol, criques secrètes accessibles à pied ou en bateau, et excursions vers les splendides îles de Port-Cros et Porquerolles, véritables joyaux de la Méditerranée.
            </p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
