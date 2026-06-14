<script setup lang="ts">
import Header from './components/Header.vue';
import Hero from './components/Hero.vue';
import CareerTimeline from './components/CareerTimeline.vue';
import WhatIDo from './components/WhatIDo.vue';
import SelectedProjects from './components/SelectedProjects.vue';
import CallToAction from './components/CallToAction.vue';
import Footer from './components/Footer.vue';
</script>

<template>
  <div class="app-layout">
    <Header />
    <main>
      <Hero />
      <CareerTimeline />
      <WhatIDo />
      <SelectedProjects />
      <CallToAction />
    </main>
    <Footer />
  </div>
</template>

<style scoped>
.app-layout {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}

main {
  flex-grow: 1;
}
</style>
