<template>
  <Navbar />

  <main class="bg-gray-50 mx-auto space-y-20">
    <Hero />
    <ImageTextSection />
    <Stats />
    <TextCards />
    <TextText />
    <Banner />
    <Testimonials />
    <Logos />
    <Contact />
    <QuestionsFrequentes />
    <Footer />
  </main>
</template>

<script setup>
import Navbar from './components/Navbar.vue'
import Hero from './components/Hero.vue'
import Images from './components/Images.vue'
import ImageTextSection from './components/ImageTextSection.vue'
import Stats from './components/Stats.vue'
import TextCards from './components/TextCards.vue'
import TextText from './components/TextText.vue'
import Testimonials from './components/Testimonials.vue'
import Logos from './components/Logos.vue'
import FullWidthSlider from './components/FullWidthSlider.vue'
import Banner from './components/Banner.vue'
import QuestionsFrequentes from './components/QuestionsFrequentes.vue'
import Contact from './components/Contact.vue'
import Footer from './components/Footer.vue'
</script>
