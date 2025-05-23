<template>
    <section class="container mx-auto px-4 py-16 max-w-[1250px]" id="lappartement">
        <FadeInOnScroll>
        <div class="flex flex-col md:flex-row gap-20 justify-center items-center">
            
            <!-- Image 1 -->
            <div class="relative w-full md:w-[520px] h-[520px] fade-in-up">
                <img src="../assets/salon.png" alt="Image 1" class="object-cover w-full h-full" />
                <div class="absolute inset-0" />
            </div>

            <!-- Image 2 -->
            <div class="relative w-full md:w-[520px] h-[520px] fade-in-up">
                <img src="../assets/terrasse.png" alt="Image 2" class="object-cover w-full h-full" />
                <div class="absolute inset-0" />
            </div>

        </div>
    </FadeInOnScroll>
    </section>
</template>

<script setup>
import FadeInOnScroll from '@/components/FadeInOnScroll.vue'
</script>