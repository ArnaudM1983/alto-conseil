<template>
    <section class="relative h-dvh flex items-end overflow-hidden">
        <!-- Image en arrière-plan -->
        <img :src="imageSrc" alt="Image de terrasse" class="absolute top-0 left-0 w-full h-full object-cover" />

        <!-- Overlay + Contenu -->
        <div class="relative z-10 w-full text-black p-8 md:p-16">
            <FadeInOnScroll>
                <h1 class="text-4xl md:text-7xl lora-font">{{ mainTitle }}</h1>
                <p class="mt-4 text-lg md:text-2xl font-thin">{{ mainParagraph }}</p>
            </FadeInOnScroll>
        </div>
    </section>
</template>


<script setup>
import { defineProps } from 'vue'
import FadeInOnScroll from '@/components/FadeInOnScroll.vue'

// Import de l'image placeholder dans /assets
import terrassePlaceholder from '@/assets/terrasse2.png'

const props = defineProps({
    imageSrc: {
        type: String,
        default: terrassePlaceholder,
    },
    mainTitle: {
        type: String,
        default: 'Titre principal',
    },
    mainParagraph: {
        type: String,
        default: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit.',
    },
})
</script>

<style scoped>
.lora-font {
    font-family: 'Lora', serif;
}
</style>