<template>
    <section class="max-w-[1250px] mx-auto text-white px-4 md:px-0" id="faq">
        <h2 class="text-3xl mb-10 md:text-6xl font-semibold text-white sm:text-3xl text-left">
            Questions Fréquentes
        </h2>

        <div class="grid grid-cols-1 md:grid-cols-12 gap-8">
            <!-- Colonne de gauche : Catégories -->
            <div class="flex flex-col space-y-4 md:col-span-5">
                <button v-for="tab in tabs" :key="tab" @click="selectedTab = tab" :class="[
                    'py-3 text-left rounded-lg transition-colors cursor-pointer text-xl md:text-4xl urbanist-font',
                    selectedTab === tab
                        ? 'text-white font-normal'
                        : 'text-gray-500 hover:text-white'
                ]">
                    {{ tab }}
                </button>
            </div>

            <!-- Colonne de droite : FAQ -->
            <div class="md:col-span-7 space-y-4">
                <div v-for="(faq, index) in faqs[selectedTab]" :key="index" class="border-b border-white pb-4">
                    <div class="flex justify-between items-center cursor-pointer text-left" @click="toggle(index)">
                        <h3 class="text-lg font-light py-4">{{ faq.question }}</h3>
                        <span class="text-xl">
                            {{ openIndex === index ? '−' : '+' }}
                        </span>
                    </div>
                    <div v-if="openIndex === index" class="mt-6 mb-2 text-gray-300 transition-all text-left">
                        {{ faq.answer }}
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script setup>
import { ref } from 'vue'

const tabs = ['Appartement', 'Location', 'Réservation']
const selectedTab = ref('Appartement')
const openIndex = ref(null)

const toggle = (index) => {
    openIndex.value = openIndex.value === index ? null : index
}

const faqs = {
    Appartement: [
        { question: 'Quelle est la superficie de l’appartement ?', answer: 'L’appartement fait 75m².' },
        { question: 'Y a-t-il une terrasse ?', answer: 'Oui, une terrasse de 20m² est disponible.' },
        { question: 'L’appartement est-il climatisé ?', answer: 'Oui, il dispose de la climatisation.' },
        { question: 'Peut-on cuisiner sur place ?', answer: 'Une cuisine équipée est à votre disposition.' },
        { question: 'Y a-t-il un ascenseur ?', answer: 'Oui, l’immeuble est équipé d’un ascenseur.' },
    ],
    Location: [
        { question: 'La location inclut-elle les charges ?', answer: 'Oui, toutes les charges sont incluses.' },
        { question: 'Les animaux sont-ils autorisés ?', answer: 'Non, les animaux ne sont pas autorisés.' },
        { question: 'Quelle est la durée minimale ?', answer: 'Le séjour minimum est de 2 nuits.' },
        { question: 'Puis-je louer pour un mois ?', answer: 'Oui, la location mensuelle est possible sur demande.' },
        { question: 'Y a-t-il un dépôt de garantie ?', answer: 'Oui, un dépôt de 300€ est requis.' },
    ],
    Réservation: [
        { question: 'Comment puis-je réserver ?', answer: 'La réservation se fait en ligne via notre site.' },
        { question: 'Quels moyens de paiement acceptez-vous ?', answer: 'Carte bancaire, PayPal et virement bancaire.' },
        { question: 'Puis-je annuler ma réservation ?', answer: 'Oui, jusqu’à 48h avant la date d’arrivée.' },
        { question: 'Recevrai-je une confirmation ?', answer: 'Oui, un email vous sera envoyé immédiatement.' },
        { question: 'Puis-je modifier mes dates ?', answer: 'Oui, selon disponibilité.' },
    ]
}
</script>


<style scoped>
.urbanist-font {
  font-family: 'Urbanist', serif;
}
</style>
