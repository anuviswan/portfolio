<script setup lang="ts">
// What I Do component - Presentational
</script>

<template>
  <section id="about" class="what-i-do-section">
    <div class="container text-center">
      <h2 class="section-title">What I Do</h2>
      <p class="section-subtitle">Architecture. Leadership. Delivery.</p>

      <div class="services-grid">
        <!-- Solution Architecture -->
        <div class="service-item">
          <div class="service-icon puzzle">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="w-8 h-8">
              <path d="M19.439 10.329C19.89 9.38 20.485 8.5 21.5 8.5a2.5 2.5 0 0 1 0 5c-1.015 0-1.61-.88-2.061-1.829a2.5 2.5 0 0 0-4.378 0c-.451.95-1.046 1.83-2.061 1.83a2.5 2.5 0 0 1 0-5c1.015 0 1.61.88 2.061 1.829a2.5 2.5 0 0 0 4.378 0Z" />
              <path d="M10.329 19.439C9.38 19.89 8.5 20.485 8.5 21.5a2.5 2.5 0 0 1-5 0c0-1.015.88-1.61 1.829-2.061a2.5 2.5 0 0 0 0-4.378c-.95-.451-1.83-1.046-1.83-2.061a2.5 2.5 0 0 1 5 0c0 1.015-.88 1.61-2.061 1.829a2.5 2.5 0 0 0 0 4.378Z" />
              <path d="M15 3h1.5a2.5 2.5 0 0 1 2.5 2.5V7" />
              <path d="M19 15v1.5A2.5 2.5 0 0 1 16.5 19H15" />
              <path d="M9 19H7.5A2.5 2.5 0 0 1 5 16.5V15" />
              <path d="M5 9V7.5A2.5 2.5 0 0 1 7.5 5H9" />
            </svg>
          </div>
          <h3 class="service-title">Solution Architecture</h3>
          <p class="service-desc">Design scalable, maintainable and evolvable software architectures.</p>
        </div>

        <!-- Platform Engineering -->
        <div class="service-item">
          <div class="service-icon layers">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="w-8 h-8">
              <polygon points="12 2 2 7 12 12 22 7 12 2" />
              <polyline points="2 17 12 22 22 17" />
              <polyline points="2 12 12 17 22 12" />
            </svg>
          </div>
          <h3 class="service-title">Platform Engineering</h3>
          <p class="service-desc">Build robust platforms and frameworks that enable product innovation.</p>
        </div>

        <!-- Technical Leadership -->
        <div class="service-item">
          <div class="service-icon people">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="w-8 h-8">
              <path d="M17 21v-2a4 4 0 0 0-4-4H5a4 4 0 0 0-4 4v2" />
              <circle cx="9" cy="7" r="4" />
              <path d="M23 21v-2a4 4 0 0 0-3-3.87" />
              <path d="M16 3.13a4 4 0 0 1 0 7.75" />
            </svg>
          </div>
          <h3 class="service-title">Technical Leadership</h3>
          <p class="service-desc">Lead engineering teams and drive quality, performance and business value.</p>
        </div>

        <!-- Modernization -->
        <div class="service-item">
          <div class="service-icon sync">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="w-8 h-8">
              <path d="M3 12a9 9 0 0 1 9-9 9.75 9.75 0 0 1 6.74 2.74L21 8" />
              <path d="M16 3h5v5" />
              <path d="M21 12a9 9 0 0 1-9 9 9.75 9.75 0 0 1-6.74-2.74L3 16" />
              <path d="M8 21H3v-5" />
            </svg>
          </div>
          <h3 class="service-title">Modernization</h3>
          <p class="service-desc">Evolve legacy systems and adopt modern technologies and practices.</p>
        </div>

        <!-- Problem Solving -->
        <div class="service-item">
          <div class="service-icon bulb">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="w-8 h-8">
              <path d="M15 14c.2-1 .7-1.7 1.5-2.5 1-.9 1.5-2.2 1.5-3.5A5 5 0 0 0 8 8c0 1 .4 2.5 1.5 3.5.7.8 1.3 1.5 1.5 2.5" />
              <path d="M9 18h6" />
              <path d="M10 22h4" />
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
  gap: 0;
}

.service-item {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  text-align: left;
  padding: 24px 32px;
  transition: var(--transition);
  position: relative;
}

.service-item:not(:last-child) {
  border-right: 1px solid var(--border);
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
  }
  
  .service-item {
    border-right: none !important;
    border-bottom: 1px solid var(--border);
    padding: 32px 24px;
  }
  
  .service-item:nth-last-child(-n+2) {
    border-bottom: none;
  }
}

@media (max-width: 576px) {
  .services-grid {
    grid-template-columns: 1fr;
  }
  
  .service-item {
    border-bottom: 1px solid var(--border);
  }
  
  .service-item:last-child {
    border-bottom: none;
  }
}
</style>
