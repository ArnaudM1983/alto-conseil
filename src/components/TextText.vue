<script setup>
import bloc1 from '@/assets/bloc1.png'

defineProps({
    title: String,
    text: String,
    link: String,
    icon: String // tu peux aussi passer un SVG inline ici ou un chemin d’image
});

const cards = [
    {
        title: "Intégrer une gamme variée d’idées",
        text: "Nous croyons que l’investissement dans des idées diverses permet d’enrichir chaque projet et de réduire la volatilité des résultats.",
        link: "#",
        icon: `<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1" stroke-linecap="round" stroke-linejoin="round" class="w-12 h-12 text-[#fe5b2c]" aria-hidden="true">
      <circle cx="12" cy="12" r="10"></circle>
      <line x1="14.31" y1="8" x2="20.05" y2="17.94"></line>
      <line x1="9.69" y1="8" x2="21.17" y2="8"></line>
      <line x1="7.38" y1="12" x2="13.12" y2="2.06"></line>
      <line x1="9.69" y1="16" x2="3.95" y2="6.06"></line>
      <line x1="14.31" y1="16" x2="2.83" y2="16"></line>
      <line x1="16.62" y1="12" x2="10.88" y2="21.94"></line>
    </svg>`
    },
    {
        title: "Offrir des résultats de la plus haute qualité",
        text: "Notre approche ne se résume pas aux chiffres. Chaque année, nous allons à la rencontre de ceux qui font vivre l’entreprise.",
        link: "#",
        icon: `<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1" stroke-linecap="round" stroke-linejoin="round" class="w-12 h-12 text-[#fe5b2c]" aria-hidden="true">
      <circle cx="12" cy="12" r="10"></circle>
      <line x1="14.31" y1="8" x2="20.05" y2="17.94"></line>
      <line x1="9.69" y1="8" x2="21.17" y2="8"></line>
      <line x1="7.38" y1="12" x2="13.12" y2="2.06"></line>
      <line x1="9.69" y1="16" x2="3.95" y2="6.06"></line>
      <line x1="14.31" y1="16" x2="2.83" y2="16"></line>
      <line x1="16.62" y1="12" x2="10.88" y2="21.94"></line>
    </svg>`
    },
    {
        title: "Croire en la force de l’implication",
        text: "Maintenir un contact étroit avec la direction et passer du temps sur le terrain nous permet d’acquérir une compréhension opérationnelle",
        link: "#",
        icon: `<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1" stroke-linecap="round" stroke-linejoin="round" class="w-12 h-12 text-[#fe5b2c]" aria-hidden="true">
      <circle cx="12" cy="12" r="10"></circle>
      <line x1="14.31" y1="8" x2="20.05" y2="17.94"></line>
      <line x1="9.69" y1="8" x2="21.17" y2="8"></line>
      <line x1="7.38" y1="12" x2="13.12" y2="2.06"></line>
      <line x1="9.69" y1="16" x2="3.95" y2="6.06"></line>
      <line x1="14.31" y1="16" x2="2.83" y2="16"></line>
      <line x1="16.62" y1="12" x2="10.88" y2="21.94"></line>
    </svg>`
    },
    {
        title: "Investir dans de solides relations",
        text: "Établir des relations de confiance avec la direction et passer du temps sur place nous permet d’approfondir notre…s",
        link: "#",
        icon: `<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1" stroke-linecap="round" stroke-linejoin="round" class="w-12 h-12 text-[#fe5b2c]" aria-hidden="true">
      <circle cx="12" cy="12" r="10"></circle>
      <line x1="14.31" y1="8" x2="20.05" y2="17.94"></line>
      <line x1="9.69" y1="8" x2="21.17" y2="8"></line>
      <line x1="7.38" y1="12" x2="13.12" y2="2.06"></line>
      <line x1="9.69" y1="16" x2="3.95" y2="6.06"></line>
      <line x1="14.31" y1="16" x2="2.83" y2="16"></line>
      <line x1="16.62" y1="12" x2="10.88" y2="21.94"></line>
    </svg>`
    },
]
</script>

<template>
    <section>
        <div class="mx-auto max-w-[1250px] px-4 py-8 sm:px-6 lg:px-0">
            <div class="grid grid-cols-1 gap-4 md:grid-cols-2 md:items-center md:gap-24">
                <div class="order-2 md:order-1">
                    <div class="max-w-lg md:max-w-none text-left">
                        <h4 class="mb-5">Une équipe experte, engagée à vos côtés</h4>
                        <h2 class="font-semibold text-white sm:text-3xl">
                            Mettre en place les bonnes solutions et méthodes.
                        </h2>
                        <p class="mt-4">
                            Notre équipe intervient sur divers marchés et compétences pour vous aider à établir une stratégie en phase avec les réalités de votre entreprise. Que vous souhaitiez améliorer la performance opérationnelle ou atténuer les risques liés aux fusions et acquisitions.
                        </p>
                        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1"
                            stroke-linecap="round" stroke-linejoin="round" xmlns="http://www.w3.org/2000/svg"
                            aria-hidden="true" class="mb-2 w-20 h-20">
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
                    <h5 class="text-left mb-6">Notre expertise va bien au-delà des chiffres. Nous ne nous contentons pas
                        de tableurs ou de visites de sites. Année après année, nous apprenons à connaître les personnes
                        qui font
                        fonctionner l’entreprise.
                    </h5>
                    <p class="text-left">
                        Nous croyons que cette approche permet non seulement de réduire les risques,
                        mais aussi de dynamiser chaque projet avec un mélange diversifié de professionnels expérimentés.
                    </p>
                </div>
            </div>
        </div>
    </section>

    <section>
        <div class="max-w-[1250px] mx-auto grid grid-cols-1 md:grid-cols-4">
            <div v-for="(card, index) in cards" :key="index"
                class="relative bg-white p-8 shadow-md flex flex-col gap-4 overflow-hidden">
                <!-- Overlay -->
                <div class="absolute inset-0 pointer-events-none" style="background: linear-gradient(86deg, #ffffff 0%, rgb(93, 93, 93) 100%);
               opacity: 0.08;"></div>

                <!-- Contenu de la carte -->
                <h6 class="text-[#fe5b2c] font-semibold mb-3 text-left relative z-10">{{ card.title }}</h6>
                <p class="text-gray-700 flex-grow mb-4 text-left relative z-10">{{ card.text }}</p>
                <a :href="card.link"
                    class="inline-flex gap-2 text-[#fe5b2c] font-semibold hover:underline items-center relative z-10">
                    Lire Plus
                    <svg class="w-4 h-4" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"
                        stroke-linecap="round" stroke-linejoin="round" aria-hidden="true">
                        <line x1="5" y1="12" x2="19" y2="12"></line>
                        <polyline points="12 5 19 12 12 19"></polyline>
                    </svg>
                </a>
                <div v-if="card.icon" v-html="card.icon" class="mt-3 text-[#fe5b2c] relative z-10"></div>
            </div>
        </div>
    </section>

</template>
