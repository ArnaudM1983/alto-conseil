<template>
    <section class="max-w-3xl mx-auto py-12 px-6">
        <h2 class="text-2xl font-semibold mb-6 text-gray-800 text-center">Questions fréquentes</h2>
        <div v-for="(faq, index) in faqs" :key="index" class="mb-4 rounded overflow-hidden">
            <div class="flex justify-between items-center p-4 cursor-pointer bg-[#f5f5f5] hover:bg-[#fe5b2c] transition-colors group"
                :class="faq.open ? 'bg-[#fe5b2c] text-white' : 'text-gray-800'" @click="toggleFAQ(index)">
                <h6 class="transition-colors" :class="{ 'text-white': faq.open }">
                    {{ faq.question }}
                </h6>
                <span class="text-2xl font-bold transition-colors group-hover:text-white"
                    :class="{ 'text-white': faq.open, 'text-[#fe5b2c]': !faq.open }">
                    {{ faq.open ? '–' : '+' }}
                </span>
            </div>

            <transition name="fade">
                <div v-show="faq.open" class="p-4 text-gray-700 bg-white  text-sm leading-relaxed text-left">
                    {{ faq.answer }}
                </div>
            </transition>
        </div>
    </section>
</template>

<script setup>
import { ref } from 'vue'

const faqs = ref([
    {
        question: 'Quels types de placements proposez-vous ?',
        answer:
            'Nous proposons des placements diversifiés : actions, obligations, immobiliers, et investissements alternatifs.',
        open: false
    },
    {
        question: 'L’accompagnement est-il personnalisé ?',
        answer:
            'Oui, chaque client bénéficie d’une analyse et de recommandations personnalisées.',
        open: false
    },
    {
        question: 'Quels sont vos frais ?',
        answer:
            'Nos frais sont transparents et indiqués dès le départ. Aucun frais caché.',
        open: false
    },
    {
        question: 'Est-ce que je peux modifier ma stratégie plus tard ?',
        answer:
            'Bien sûr. Vous pouvez adapter votre stratégie à tout moment selon vos objectifs.',
        open: false
    },
    {
        question: 'Proposez-vous un suivi régulier ?',
        answer:
            'Nous proposons un suivi continu avec des bilans réguliers pour ajuster votre portefeuille.',
        open: false
    }
])

function toggleFAQ(index) {
    faqs.value[index].open = !faqs.value[index].open
}
</script>

<style scoped>
.fade-enter-active,
.fade-leave-active {
    transition: all 0.3s ease;
}

.fade-enter-from,
.fade-leave-to {
    opacity: 0;
    transform: translateY(-5px);
}

.group:hover h6 {
  color: white;
}
</style>