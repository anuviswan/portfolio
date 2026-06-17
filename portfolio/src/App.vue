<script setup lang="ts">
import Header from './components/Header.vue';
import Hero from './components/Hero.vue';
import ProfessionalPresence from './components/ProfessionalPresence.vue';
import CareerTimeline from './components/CareerTimeline.vue';
import WhatIDo from './components/WhatIDo.vue';
import SelectedProjects from './components/SelectedProjects.vue';
import CallToAction from './components/CallToAction.vue';
import Footer from './components/Footer.vue';

const showSelectedProjects = import.meta.env.VITE_SHOW_SELECTED_PROJECTS !== 'false';
</script>

<template>
  <div class="app-layout">
    <Header />
    <main>
      <Hero />
      <ProfessionalPresence />
      <CareerTimeline />
      <WhatIDo />
      <SelectedProjects v-if="showSelectedProjects" />
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
