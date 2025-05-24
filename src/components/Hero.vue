<template>
    <section class="relative h-dvh overflow-hidden ">
        <!-- Image en arrière-plan -->
        <img :src="imageSrc" alt="Image de terrasse" class="absolute top-0 left-0 w-full h-full object-cover" />

        <!-- Overlay -->
        <div class="absolute inset-0 z-0 pointer-events-none" :style="{
            background: 'linear-gradient(to bottom left, rgba(232,79,36,1) 0%, rgba(34,34,34,0.5) 51%, transparent 90%)',
        }" aria-hidden="true"></div>

        <!-- Contenu en deux colonnes -->
        <div class="relative z-10 flex flex-col md:flex-row items-center h-full ">
            <!-- Colonne gauche (60%) -->
            <div class="w-full md:w-4/6 p-8 md:p-16 flex flex-col justify-end text-left text-black">
                <FadeInOnScroll>
                    <h1 class="text-3xl md:text-5xl mb-16">{{ mainTitle }}</h1>
                    <h3 class="mt-4 text-lg md:text-xl font-thin text-white uppercase">{{ mainParagraph }}</h3>
                    <a href="#"
                        class="inline-block mt-10 bg-white text-orange-500 px-8 py-4 font-dm text-lg leading-6 transition duration-200 hover:bg-[#e14e26] hover:text-white">
                        Voir Nos Expertises
                    </a>
                </FadeInOnScroll>
            </div>

            <!-- Colonne droite (40%) - facultative -->
            <div class="hidden md:block md:w-1/6"></div>
        </div>
    </section>
</template>


<script setup>
import { defineProps } from 'vue'
import FadeInOnScroll from '@/components/FadeInOnScroll.vue'
import terrassePlaceholder from '@/assets/hero-bg.png'

const props = defineProps({
    imageSrc: {
        type: String,
        default: terrassePlaceholder,
    },
    mainTitle: {
        type: String,
        default: 'Libérez le potentiel de votre entreprise',
    },
    mainParagraph: {
        type: String,
        default: 'Conseil en stratégie, transformation digitale et performance opérationnelle',
    },
})
</script>

<style scoped>
.lora-font {
    font-family: 'Lora', serif;
}
</style>