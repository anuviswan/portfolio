<script setup lang="ts">
import domainsData from '../data/domain.json';

const getDomainIcon = (domainName: string) => {
  const norm = domainName.toLowerCase();
  if (norm.includes('life science') || norm.includes('laboratory') || norm.includes('pharmaceutical')) {
    return 'flask';
  } else if (norm.includes('surface') || norm.includes('analytical') || norm.includes('scientific') || norm.includes('measurement')) {
    return 'science';
  } else if (norm.includes('industrial') || norm.includes('manufacturing') || norm.includes('analytics')) {
    return 'automation';
  } else if (norm.includes('healthcare') || norm.includes('clinical') || norm.includes('dispensing')) {
    return 'healthcare';
  }
  return 'flask';
};
</script>

<template>
  <section id="home" class="hero-section">
    <div class="bg-grid-pattern"></div>
    <div class="dot-decor top-left-decor"></div>
    <div class="dot-decor bottom-right-decor"></div>
    
    <div class="container hero-container">
      <div class="hero-left">
        <span class="hero-tag">LEAD SOFTWARE ARCHITECT</span>
        <h1 class="hero-title">
          Building Software That <br />
          <span class="highlight">Solves Real Problems</span>
        </h1>
        <p class="hero-desc">
          With 20+ years of experience designing and delivering scientific, industrial, healthcare and enterprise software systems that drive real impact.
        </p>

        <div class="stats-grid">
          <div class="stat-item">
            <div class="stat-icon">
              <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" d="M17.25 6.75L22.5 12l-5.25 5.25m-10.5 0L1.5 12l5.25-5.25m7.5-3l-4.5 16.5" />
              </svg>
            </div>
            <div class="stat-info">
              <span class="stat-value">20+</span>
              <span class="stat-label">Years Experience</span>
            </div>
          </div>
          <div class="stat-item">
            <div class="stat-icon">
              <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" d="M18 18.72a9.094 9.094 0 003.741-.479 3 3 0 00-4.682-2.72m.94 3.198l.001.031c0 .225-.012.447-.037.666A11.944 11.944 0 0112 21c-2.17 0-4.207-.576-5.963-1.584A6.062 6.062 0 016 18.719m12 0a5.971 5.971 0 00-.941-3.197m0 0A5.995 5.995 0 0012 12.75a5.995 5.995 0 00-5.058 2.772m0 0a3 3 0 00-4.681 2.72 8.986 8.986 0 003.74.477m.94-3.197a5.971 5.971 0 00-.94 3.197M15 6.75a3 3 0 11-6 0 3 3 0 016 0zm6 3a2.25 2.25 0 11-4.5 0 2.25 2.25 0 014.5 0zm-13.5 0a2.25 2.25 0 11-4.5 0 2.25 2.25 0 014.5 0z" />
              </svg>
            </div>
            <div class="stat-info">
              <span class="stat-value">4</span>
              <span class="stat-label">Organizations</span>
            </div>
          </div>
          <div class="stat-item">
            <div class="stat-icon">
              <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" d="M12 21a9.004 9.004 0 008.716-6.747M12 21a9.004 9.004 0 01-8.716-6.747M12 21c2.485 0 4.5-4.03 4.5-9S14.485 3 12 3m0 18c-2.485 0-4.5-4.03-4.5-9S9.515 3 12 3m0 0a8.997 8.997 0 017.843 4.582M12 3a8.997 8.997 0 00-7.843 4.582m15.686 0A11.953 11.953 0 0112 10.5c-2.998 0-5.74-1.1-7.843-2.918m15.686 0A8.959 8.959 0 0121 12c0 .778-.099 1.533-.284 2.253m0 0A17.919 17.919 0 0112 16.5c-3.162 0-6.133-.815-8.716-2.247m0 0A9.015 9.015 0 013 12c0-.778.099-1.533.284-2.253" />
              </svg>
            </div>
            <div class="stat-info">
              <span class="stat-value">Global</span>
              <span class="stat-label">Client Collaboration</span>
            </div>
          </div>
          <div class="stat-item">
            <div class="stat-icon">
              <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" d="M12 18a3.75 3.75 0 00.495-7.467 5.99 5.99 0 00-1.925 3.546 5.974 5.974 0 01-2.133-1A3.75 3.75 0 0012 18z" />
                <path stroke-linecap="round" stroke-linejoin="round" d="M12 3v1m0 16v1m9-9h-1M4 12H3m15.364-6.364l-.707.707M6.343 17.657l-.707.707m0-12.728l.707.707m11.314 11.314l.707.707M12 5a7 7 0 100 14 7 7 0 000-14z" />
              </svg>
            </div>
            <div class="stat-info">
              <span class="stat-value">Multiple</span>
              <span class="stat-label">Domains</span>
            </div>
          </div>
        </div>

        <div class="hero-actions">
          <a href="#projects" class="btn btn-primary">
            <span>View My Work</span>
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2.5" stroke="currentColor" class="btn-arrow w-4 h-4">
              <path stroke-linecap="round" stroke-linejoin="round" d="M13.5 4.5L21 12m0 0l-7.5 7.5M21 12H3" />
            </svg>
          </a>
          <a href="#contact" class="btn btn-outline">
            <span>Contact Me</span>
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" class="w-4 h-4">
              <path stroke-linecap="round" stroke-linejoin="round" d="M21.75 6.75v10.5a2.25 2.25 0 01-2.25 2.25h-15a2.25 2.25 0 01-2.25-2.25V6.75m19.5 0A2.25 2.25 0 0019.5 4.5h-15a2.25 2.25 0 00-2.25 2.25m19.5 0v.243a2.25 2.25 0 01-1.07 1.916l-7.5 4.615a2.25 2.25 0 01-2.36 0L3.32 8.91a2.25 2.25 0 01-1.07-1.916V6.75" />
            </svg>
          </a>
        </div>
      </div>

      <div class="hero-right">
        <div class="quote-card">
          <div class="quote-mark">“</div>
          <p class="quote-text">
            I enjoy solving complex problems, designing clean architectures, mentoring teams and delivering value through technology.
          </p>
        </div>

        <div class="domains-card">
          <h3 class="domains-title">My Domains</h3>
          <div class="domains-list">
            <div 
              v-for="item in domainsData.domains" 
              :key="item.domain" 
              class="domain-item"
            >
              <div class="domain-icon" :class="getDomainIcon(item.domain)">
                <!-- Flask Icon -->
                <svg v-if="getDomainIcon(item.domain) === 'flask'" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" d="M9.75 3.104v13.01a4.5 4.5 0 001.072 2.913l2.056 2.467A.75.75 0 0014 21.3V3.104M9.75 3.104c-.394.025-.783.085-1.166.177M9.75 3.104h4.5M14 3.104c.394.025.783.085 1.166.177m0 0a12.062 12.062 0 01-2.332.354M9.003 20.162A9.003 9.003 0 019 18v-4.5m6 4.5c0 .733-.088 1.445-.253 2.128M9.75 16.5h4.5" />
                </svg>

                <!-- Microscope / Science Icon -->
                <svg v-else-if="getDomainIcon(item.domain) === 'science'" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" d="M6 18h12M12 18v3m0-6v-3m0 0a3 3 0 10-6 0v3m6-3h3.5a1.5 1.5 0 011.5 1.5V18M10 9l4 2.5M12 4.5a2.5 2.5 0 10-5 0v3h5v-3z" />
                </svg>

                <!-- Gear / Automation Icon -->
                <svg v-else-if="getDomainIcon(item.domain) === 'automation'" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" d="M9.594 3.94c.09-.542.56-.94 1.11-.94h2.593c.55 0 1.02.398 1.11.94l.213 1.281c.063.374.313.686.645.87.074.04.147.083.22.127.324.196.72.257 1.075.124l1.217-.456a1.125 1.125 0 011.37.49l1.296 2.247a1.125 1.125 0 01-.26 1.43l-1.003.828c-.293.241-.438.613-.43 1 .002.044.004.088.004.132 0 .044-.002.088-.004.132-.008.387.137.759.43 1l1.003.828c.427.352.536.953.26 1.43l-1.296 2.247a1.125 1.125 0 01-1.37.49l-1.216-.456c-.356-.133-.751-.072-1.076.124a6.57 6.57 0 01-.22.128c-.331.183-.581.495-.644.869l-.213 1.28c-.09.543-.56.94-1.11.94h-2.594c-.55 0-1.02-.398-1.11-.94l-.213-1.281c-.062-.374-.312-.686-.644-.87a6.52 6.52 0 01-.22-.127c-.325-.196-.72-.257-1.076-.124l-1.217.456a1.125 1.125 0 01-1.369-.49l-1.297-2.247a1.125 1.125 0 01.26-1.43l1.004-.827c.292-.24.437-.613.43-1a6.9 6.9 0 01-.004-.133c0-.044.002-.088.004-.132.008-.387-.138-.76-.43-1l-1.004-.828a1.125 1.125 0 01-.26-1.43l1.297-2.247a1.125 1.125 0 011.37-.49l1.216.456c.356.133.751.072 1.076-.124.072-.044.146-.087.22-.128.332-.183.582-.495.645-.869l.214-1.28z" />
                  <path stroke-linecap="round" stroke-linejoin="round" d="M15 12a3 3 0 11-6 0 3 3 0 016 0z" />
                </svg>

                <!-- Healthcare Icon -->
                <svg v-else-if="getDomainIcon(item.domain) === 'healthcare'" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" d="M21 8.25c0-2.485-2.099-4.5-4.688-4.5-1.935 0-3.597 1.126-4.312 2.733-.715-1.607-2.377-2.733-4.313-2.733C5.1 3.75 3 5.765 3 8.25c0 7.22 9 12 9 12s9-4.78 9-12z" />
                </svg>
              </div>
              <div class="domain-info">
                <h4 class="domain-name">{{ item.domain }}</h4>
                <p class="domain-desc">{{ item.description }}</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.hero-section {
  position: relative;
  overflow: hidden;
  padding: 100px 0 80px;
  border-bottom: 1px solid var(--border);
}

.hero-container {
  display: grid;
  grid-template-columns: 1.1fr 0.9fr;
  gap: 48px;
  align-items: flex-start;
  position: relative;
  z-index: 10;
}

.hero-left {
  display: flex;
  flex-direction: column;
  text-align: left;
}

.hero-tag {
  color: var(--primary);
  font-family: var(--font-heading);
  font-weight: 700;
  font-size: 0.85rem;
  letter-spacing: 0.15em;
  margin-bottom: 16px;
}

.hero-title {
  font-size: 3.25rem;
  font-weight: 700;
  line-height: 1.15;
  margin-bottom: 24px;
  color: var(--navy);
}

.highlight {
  color: var(--primary);
}

.hero-desc {
  font-size: 1.15rem;
  color: var(--text-secondary);
  margin-bottom: 40px;
  max-width: 540px;
}

.stats-grid {
  display: flex;
  flex-wrap: wrap;
  gap: 32px;
  margin-bottom: 40px;
}

.stat-item {
  display: flex;
  align-items: flex-start;
  gap: 12px;
}

.stat-icon {
  color: var(--primary);
  opacity: 0.85;
  padding-top: 2px;
  flex-shrink: 0;
}

.stat-icon svg {
  width: 24px;
  height: 24px;
}

.stat-info {
  display: flex;
  flex-direction: column;
}

.stat-value {
  font-family: var(--font-heading);
  font-size: 1.35rem;
  font-weight: 700;
  color: var(--navy);
  line-height: 1.2;
}

.stat-label {
  font-size: 0.85rem;
  color: var(--text-muted);
}

.hero-actions {
  display: flex;
  gap: 16px;
}

.btn-arrow {
  transition: transform 0.2s;
}

.btn:hover .btn-arrow {
  transform: translateX(4px);
}

.hero-right {
  display: flex;
  flex-direction: column;
  gap: 24px;
  align-items: flex-end;
}

.quote-card {
  background: var(--bg-main);
  border: 1px solid var(--border);
  box-shadow: var(--shadow-lg);
  border-radius: var(--radius-lg);
  padding: 36px;
  width: 100%;
  max-width: 440px;
  text-align: left;
  position: relative;
}

.quote-mark {
  font-family: var(--font-heading);
  font-size: 5rem;
  color: var(--primary);
  opacity: 0.15;
  position: absolute;
  top: 8px;
  left: 24px;
  line-height: 0;
}

.quote-text {
  font-size: 1.05rem;
  font-style: italic;
  color: var(--text-secondary);
  line-height: 1.6;
  position: relative;
  z-index: 5;
}

.domains-card {
  background: var(--bg-main);
  border: 1px solid var(--border);
  box-shadow: var(--shadow-lg);
  border-radius: var(--radius-lg);
  padding: 36px;
  width: 100%;
  max-width: 440px;
  text-align: left;
}

.domains-title {
  font-size: 1.2rem;
  font-weight: 700;
  color: var(--navy);
  margin-bottom: 24px;
  font-family: var(--font-heading);
}

.domains-list {
  display: flex;
  flex-direction: column;
  gap: 20px;
}

.domain-item {
  display: flex;
  align-items: flex-start;
  gap: 16px;
}

.domain-icon {
  width: 40px;
  height: 40px;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-shrink: 0;
}

.domain-icon svg {
  width: 20px;
  height: 20px;
}

.domain-icon.flask,
.domain-icon.automation,
.domain-icon.healthcare,
.domain-icon.enterprise {
  background-color: #f0fdfa;
  color: #0d9488;
}

.domain-info {
  display: flex;
  flex-direction: column;
}

.domain-name {
  font-weight: 600;
  font-size: 0.95rem;
  color: var(--text-primary);
  font-family: var(--font-heading);
  margin-bottom: 2px;
}

.domain-desc {
  font-size: 0.85rem;
  color: var(--text-muted);
  line-height: 1.4;
}

.top-left-decor {
  position: absolute;
  top: 20px;
  left: 20px;
}

.bottom-right-decor {
  position: absolute;
  bottom: 20px;
  right: 20px;
}

@media (max-width: 992px) {
  .hero-container {
    grid-template-columns: 1fr;
    gap: 40px;
  }
  
  .hero-right {
    align-items: center;
  }
  
  .quote-card, .domains-card {
    max-width: 100%;
  }
}
</style>
