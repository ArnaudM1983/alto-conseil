<template>
  <Navbar />

  <main class="bg-neutral-200 mx-auto space-y-20">
    <Hero />
    <Images />
    <Marquee />
    <ImageTextSection />
    <FullWidthSlider />
    <Map />
    <Equipement />
    <Banner />
    <QuestionsFrequentes />
    <Contact />
    <ScrollingBanner />
    <Footer />
  </main>
</template>

<script setup>
import Navbar from './components/Navbar.vue'
import Hero from './components/Hero.vue'
import Images from './components/Images.vue'
import Marquee from './components/Marquee.vue'
import ImageTextSection from './components/ImageTextSection.vue'
import FullWidthSlider from './components/FullWidthSlider.vue'
import Map from './components/Map.vue'
import Equipement from './components/Equipement.vue'
import Banner from './components/Banner.vue'
import QuestionsFrequentes from './components/QuestionsFrequentes.vue'
import Contact from './components/Contact.vue'
import ScrollingBanner from './components/ScrollingBanner.vue'
import Footer from './components/Footer.vue'
</script>
