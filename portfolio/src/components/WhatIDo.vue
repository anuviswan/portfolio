<script setup lang="ts">
// What I Do component - Presentational
</script>

<template>
  <section class="what-i-do-section">
    <div class="container text-center">
      <h2 class="section-title">What I Do</h2>
      <p class="section-subtitle">Architecture. Leadership. Delivery.</p>

      <div class="services-grid">
        <!-- Solution Architecture -->
        <div class="service-item">
          <div class="service-icon puzzle">
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" class="w-8 h-8">
              <path stroke-linecap="round" stroke-linejoin="round" d="M14.25 9.75L16.5 12l-2.25 2.25m-4.5 0L7.5 12l2.25-2.25M6 20.25h12A2.25 2.25 0 0020.25 18V6A2.25 2.25 0 0018 3.75H6A2.25 2.25 0 003.75 6v12A2.25 2.25 0 006 20.25z" />
            </svg>
          </div>
          <h3 class="service-title">Solution Architecture</h3>
          <p class="service-desc">Design scalable, maintainable and evolvable software architectures.</p>
        </div>

        <!-- Platform Engineering -->
        <div class="service-item">
          <div class="service-icon layers">
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" class="w-8 h-8">
              <path stroke-linecap="round" stroke-linejoin="round" d="M6.429 9.75L2.25 12l4.179 2.25m11.142 0L21.75 12l-4.179-2.25M12 5.75v12.5M3.75 18h16.5M3.75 6h16.5" />
            </svg>
          </div>
          <h3 class="service-title">Platform Engineering</h3>
          <p class="service-desc">Build robust platforms and frameworks that enable product innovation.</p>
        </div>

        <!-- Technical Leadership -->
        <div class="service-item">
          <div class="service-icon people">
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" class="w-8 h-8">
              <path stroke-linecap="round" stroke-linejoin="round" d="M18 18.72a9.094 9.094 0 003.741-.479 3 3 0 00-4.682-2.72m.94 3.198l.001.031c0 .225-.012.447-.037.666A11.944 11.944 0 0112 21c-2.17 0-4.207-.576-5.963-1.584A6.062 6.062 0 016 18.719m12 0a5.971 5.971 0 00-.941-3.197m0 0A5.995 5.995 0 0012 12.75a5.995 5.995 0 00-5.058 2.772m0 0a3 3 0 00-4.681 2.72 8.986 8.986 0 003.74.477m.94-3.197a5.971 5.971 0 00-.94 3.197M15 6.75a3 3 0 11-6 0 3 3 0 016 0zm6 3a2.25 2.25 0 11-4.5 0 2.25 2.25 0 014.5 0zm-13.5 0a2.25 2.25 0 11-4.5 0 2.25 2.25 0 014.5 0z" />
            </svg>
          </div>
          <h3 class="service-title">Technical Leadership</h3>
          <p class="service-desc">Lead engineering teams and drive quality, performance and growth.</p>
        </div>

        <!-- Modernization -->
        <div class="service-item">
          <div class="service-icon sync">
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" class="w-8 h-8">
              <path stroke-linecap="round" stroke-linejoin="round" d="M16.023 9.348h4.992v-.001M2.985 19.644v-4.992m0 0h4.992m-4.993 0l3.181 3.183a8.25 8.25 0 0013.803-3.7M4.031 9.865a8.25 8.25 0 0113.803-3.7l3.181 3.182m0-4.991v4.99" />
            </svg>
          </div>
          <h3 class="service-title">Modernization</h3>
          <p class="service-desc">Evolve legacy systems and adopt modern technologies and practices.</p>
        </div>

        <!-- Problem Solving -->
        <div class="service-item">
          <div class="service-icon bulb">
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" class="w-8 h-8">
              <path stroke-linecap="round" stroke-linejoin="round" d="M12 18a3.75 3.75 0 00.495-7.467 5.99 5.99 0 00-1.925 3.546 5.974 5.974 0 01-2.133-1A3.75 3.75 0 0012 18z" />
              <path stroke-linecap="round" stroke-linejoin="round" d="M12 3v1m0 16v1m9-9h-1M4 12H3m15.364-6.364l-.707.707M6.343 17.657l-.707.707m0-12.728l.707.707m11.314 11.314l.707.707M12 5a7 7 0 100 14 7 7 0 000-14z" />
            </svg>
          </div>
          <h3 class="service-title">Problem Solving</h3>
          <p class="service-desc">Tackle complex challenges and deliver practical, effective solutions.</p>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.what-i-do-section {
  padding: 80px 0;
  background-color: var(--bg-main);
  border-bottom: 1px solid var(--border);
}

.text-center {
  text-align: center;
}

.section-title {
  margin-bottom: 12px;
}

.section-subtitle {
  color: var(--text-muted);
  margin-bottom: 64px;
  font-size: 1.05rem;
}

.services-grid {
  display: grid;
  grid-template-columns: repeat(5, 1fr);
  gap: 24px;
}

.service-item {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  text-align: left;
  padding: 24px;
  border-radius: var(--radius-md);
  transition: var(--transition);
}

.service-item:hover {
  background-color: var(--bg-alt);
}

.service-icon {
  width: 48px;
  height: 48px;
  color: var(--primary);
  margin-bottom: 24px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.service-title {
  font-size: 1.15rem;
  font-weight: 700;
  color: var(--navy);
  margin-bottom: 12px;
  font-family: var(--font-heading);
}

.service-desc {
  font-size: 0.9rem;
  color: var(--text-secondary);
  line-height: 1.5;
}

@media (max-width: 992px) {
  .services-grid {
    grid-template-columns: repeat(2, 1fr);
    gap: 32px;
  }
}

@media (max-width: 576px) {
  .services-grid {
    grid-template-columns: 1fr;
    gap: 32px;
  }
}
</style>
