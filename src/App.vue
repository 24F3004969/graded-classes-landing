
<script setup>
import HeaderNav from './components/HeaderNav.vue';
import HeroSection from './components/HeroSection.vue';
import Categories from './components/Categories.vue';
import FeatureBanner from './components/FeatureBanner.vue';
import StatsBar from './components/StatsBar.vue';
import Instructors from './components/Instructors.vue';
import Testimonials from './components/Testimonials.vue';
import CTA from './components/CTA.vue';
import FooterBar from './components/FooterBar.vue';
</script>

<template>
  <HeaderNav />

  <main>
    <HeroSection />
    <section id="categories" class="section">
      <div class="container">
        <Categories />
      </div>
    </section>

    <section class="section-contrast section">
      <div class="container grid grid-2">
        <FeatureBanner />
      </div>
    </section>

    <section class="section">
      <div class="container">
        <StatsBar />
      </div>
    </section>

    <section id="instructors" class="section">
      <div class="container">
        <Instructors />
      </div>
    </section>

    <section id="testimonials" class="section-contrast section">
      <div class="container">
        <Testimonials />
      </div>
    </section>

    <section class="section">
      <div class="container">
        <CTA />
      </div>
    </section>
  </main>

  <FooterBar />
</template>

<style scoped>
main{overflow:hidden}
</style>
