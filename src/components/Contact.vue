<script setup>
import { ref } from 'vue'

// Données FAQ dynamiques
const faqs = ref([
    {
        question: 'Diversité d\'approches pour vos placements',
        answer:
            'Nous croyons en la diversité d’approches pour optimiser vos placements. Chaque investisseur a des objectifs, un profil de risque et un horizon différents. C’est pourquoi nous analysons une large gamme de solutions – traditionnelles ou innovantes – pour construire une stratégie d’investissement sur mesure. Cette approche nous permet de sécuriser vos intérêts tout en identifiant les meilleures opportunités de croissance.',
        open: true
    },
    {
        question: 'Un accompagnement pour prendre des décisions financières éclairées',
        answer:
            'Nous vous offrons un accompagnement personnalisé pour vous aider à comprendre vos options, clarifier vos objectifs et prendre des décisions financières réfléchies. Grâce à nos conseils, vous bénéficiez d’une vision claire et adaptée à votre situation.',
        open: false
    },
    {
        question: 'Aucun frai caché, aucun engagement',
        answer: 'Transparence et simplicité sont au cœur de notre approche. Aucun frais caché ne vous sera facturé, et vous n’êtes soumis à aucun engagement contraignant. Vous gardez le contrôle à chaque étape.',
        open: false
    },
])

// Fonction pour toggle une question
function toggleFAQ(index) {
    faqs.value[index].open = !faqs.value[index].open
}
</script>

<template>
    <section id="contact" class="mb-0">
        <div class="container px-6 mx-auto">
            <div class="lg:flex lg:items-start lg:gap-12">
                <!-- FAQ -->
                <div class="container px-6 py-12 mx-auto">
                    <h2 class="text-2xl text-left font-semibold text-gray-800 lg:text-3xl">Discutez avec l’un de nos
                        conseillers et obtenez des conseils gratuits !</h2>
                    <hr class="my-6 border-gray-200" />

                    <div v-for="(faq, index) in faqs" :key="index" class="mb-6">
                        <button @click="toggleFAQ(index)" class="flex items-center w-full text-left focus:outline-none">
                            <svg v-if="faq.open" class="w-6 h-6 text-blue-500" fill="none" viewBox="0 0 24 24"
                                stroke="currentColor">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M20 12H4" />
                            </svg>
                            <svg v-else class="w-6 h-6 text-blue-500" fill="none" viewBox="0 0 24 24"
                                stroke="currentColor">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                    d="M12 4v16m8-8H4" />
                            </svg>

                            <h6 class="mx-4 text-xl text-gray-700">{{ faq.question }}</h6>
                        </button>

                        <transition name="fade">
                            <div v-show="faq.open" class="flex mt-4 md:mx-10">
                                <span class="border-l-2 border-blue-500 mr-4"></span>
                                <p class="text-left max-w-3xl text-gray-600">{{ faq.answer }}</p>
                            </div>
                        </transition>

                        <hr class="mt-6 border-gray-200" />
                    </div>
                </div>

                <!-- Formulaire -->
                <div class="lg:w-1/2">
                    <div
                        class="w-full px-8 py-10 mx-auto overflow-hidden bg-gray-900 rounded-lg shadow-2xl lg:max-w-xl shadow-gray-300/50">
                        <p class="text-lg font-medium text-left title-contact">
                            Intéressé par une collaboration ou des questions ? Remplissez simplement le formulaire et
                            nous vous rappellerons.
                        </p>

                        <form class="mt-6">
                            <div class="flex-1">
                                <label class="block mb-2 text-sm text-gray-300 text-left">Votre Nom</label>
                                <input type="text"
                                    class="w-full px-6 py-2 text-white border border-gray-400 bg-transparent placeholder-gray-300 focus:outline-none focus:border-white" />
                            </div>

                            <div class="flex-1 mt-6">
                                <label class="block mb-2 text-sm text-gray-300 text-left">Adresse Email</label>
                                <input type="email"
                                    class="w-full px-6 py-2 text-white border border-gray-400 bg-transparent placeholder-gray-300 focus:outline-none focus:border-white" />
                            </div>

                            <div class="w-full mt-6">
                                <label class="block mb-2 text-sm text-gray-300 text-left">Votre Message</label>
                                <textarea
                                    class="w-full px-6 py-2 text-white border border-gray-400 bg-transparent placeholder-gray-300 focus:outline-none focus:border-white"></textarea>
                            </div>

                            <button
                                class="w-full text-white border border-white mt-8 px-6 py-2 hover:bg-white hover:text-black transition">
                                Soumettre le formulaire
                            </button>
                        </form>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<style scoped>
.fade-enter-active,
.fade-leave-active {
    transition: all 0.3s ease;
}

.fade-enter-from,
.fade-leave-to {
    opacity: 0;
    transform: translateY(-10px);
}

.title-contact {
    color: white;
}
</style>
