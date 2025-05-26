<script setup>
const cards = [
    {
        icon: `<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" xmlns="http://www.w3.org/2000/svg" aria-hidden="true" class="w-8 h-8 text-[#fe5b2c]">
      <circle cx="12" cy="12" r="10"></circle>
      <polyline points="12 6 12 12 16 14"></polyline>
    </svg>`,
        title: "Stratégie d’entreprise",
        text: "Définir une vision claire pour guider la croissance."
    },
    {
        icon: `<svg viewBox="0 0 640 512" fill="#fe5b2c" xmlns="http://www.w3.org/2000/svg" aria-hidden="true" class="w-8 h-8">
      <path d="M624 416H381.54c-.74 19.81-14.71 32-32.74 32H288c-18.69 0-33.02-17.47-32.77-32H16c-8.8 0-16 7.2-16 16v16c0 35.2 28.8 64 64 64h512c35.2 0 64-28.8 64-64v-16c0-8.8-7.2-16-16-16zM576 48c0-26.4-21.6-48-48-48H112C85.6 0 64 21.6 64 48v336h512V48zm-64 272H128V64h384v256z"/>
    </svg>`,
        title: "Pilotage financier",
        text: "Contrôler la rentabilité et sécuriser la gestion financière."
    },
    {
        icon: `<svg viewBox="0 0 384 512" fill="#fe5b2c" xmlns="http://www.w3.org/2000/svg" aria-hidden="true" class="w-8 h-8">
      <path d="M384 112v352c0 26.51-21.49 48-48 48H48c-26.51 0-48-21.49-48-48V112c0-26.51 21.49-48 48-48h80c0-35.29 28.71-64 64-64s64 28.71 64 64h80c26.51 0 48 21.49 48 48zM192 40c-13.255 0-24 10.745-24 24s10.745 24 24 24 24-10.745 24-24-10.745-24-24-24m96 114v-20a6 6 0 0 0-6-6H102a6 6 0 0 0-6 6v20a6 6 0 0 0 6 6h180a6 6 0 0 0 6-6z"/>
    </svg>`,
        title: "Organisation & process",
        text: "Optimiser les processus pour plus d’efficacité opérationnelle."
    }
]
</script>

<template>
    <section class="bg-gray-100" id="expertises">
        <div class="mx-auto max-w-[1250px] px-4 py-25 sm:px-6 lg:px-0">
            <div class="flex flex-col md:flex-row md:items-start md:gap-6">
                <!-- Texte à gauche - 1/3 sur desktop -->
                <div class="w-full md:w-1/3 order-1 md:order-1 mb-10 md:mb-0">
                    <div class="max-w-lg md:max-w-none text-left">
                        <h2 class="font-semibold text-white sm:text-3xl">
                            Nos domaines d’intervention
                        </h2>
                        <p class="mt-4">
                            Des conseils sur-mesure pour accompagner votre croissance et optimiser vos performances.
                        </p>
                        <div class="mt-12 w-1/2 h-2 bg-[#fe5b2c]"></div>
                    </div>
                </div>

                <!-- Cartes à droite - 2/3 sur desktop, cartes en ligne -->
                <div
                    class="w-full md:w-2/3 order-2 md:order-2 flex flex-col md:flex-row md:space-x-8 space-y-8 md:space-y-0">
                    <div v-for="(card, index) in cards" :key="index"
                        class="flex flex-col bg-white p-6 rounded shadow-md md:flex-1 gap-3 rounded-2xl">
                        <div v-html="card.icon" class="flex-shrink-0 mb-6"></div>
                        <h3 class="font-semibold text-lg text-left">{{ card.title }}</h3>
                        <p class="text-gray-700 text-left">{{ card.text }}</p>
                    </div>

                </div>
            </div>
        </div>
    </section>
</template>
