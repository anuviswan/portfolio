<script setup lang="ts">
import { computed } from 'vue';
import careerData from '../data/career.json';

const sortedCareer = computed(() => {
  return [...careerData.career].sort((a, b) => {
    const yearA = parseInt(a.period.split('-')[0].trim()) || 0;
    const yearB = parseInt(b.period.split('-')[0].trim()) || 0;
    return yearB - yearA;
  });
});

// We map each career history item index to custom theme configurations (colors, icons) to match main.png
const getTimelineTheme = (companyName: string) => {
  const norm = companyName.toLowerCase();
  if (norm.includes('calpine')) {
    return {
      color: '#0d9488',
      bgLight: '#f0fdfa',
      icon: 'flask'
    };
  } else if (norm.includes('cascade')) {
    return {
      color: '#2563eb',
      bgLight: '#eff6ff',
      icon: 'heartbeat'
    };
  } else if (norm.includes('ecsolvo')) {
    return {
      color: '#7c3aed',
      bgLight: '#f5f3ff',
      icon: 'rocket'
    };
  } else if (norm.includes('beo')) {
    return {
      color: '#ea580c',
      bgLight: '#fff7ed',
      icon: 'chart'
    };
  } else {
    // KRÜSS or default
    return {
      color: '#16a34a',
      bgLight: '#f0fdf4',
      icon: 'microscope'
    };
  }
};
</script>

<template>
  <section id="experience" class="timeline-section">
    <div class="container text-center">
      <h2 class="section-title">Career Highlights</h2>
      <p class="section-subtitle">A journey across industries and technologies</p>
      
      <div class="timeline-container">
        <!-- Horizontal Line -->
        <div class="timeline-line"></div>
        
        <div class="timeline-grid" :style="{ gridTemplateColumns: `repeat(${sortedCareer.length}, 1fr)` }">
          <div 
            v-for="job in sortedCareer" 
            :key="job.company" 
            class="timeline-card-wrapper"
            :style="{ '--accent-color': getTimelineTheme(job.company).color }"
          >
            <!-- Timeline Node Point -->
            <div class="timeline-node">
              <div class="node-dot"></div>
            </div>

            <!-- Card Body -->
            <div class="timeline-card">
              <span class="period">{{ job.period }}</span>
              <h3 class="company">{{ job.company }}</h3>
              <p class="role">{{ job.title }}</p>
              <p class="domain">{{ job.domain }}</p>
              
              <div 
                class="card-icon" 
                :style="{ 
                  backgroundColor: getTimelineTheme(job.company).bgLight,
                  color: getTimelineTheme(job.company).color 
                }"
              >
                <!-- Flask -->
                <svg v-if="getTimelineTheme(job.company).icon === 'flask'" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" class="w-6 h-6">
                  <path stroke-linecap="round" stroke-linejoin="round" d="M9.75 3.104v13.01a4.5 4.5 0 001.072 2.913l2.056 2.467A.75.75 0 0014 21.3V3.104M9.75 3.104c-.394.025-.783.085-1.166.177M9.75 3.104h4.5M14 3.104c.394.025.783.085 1.166.177m0 0a12.062 12.062 0 01-2.332.354M9.003 20.162A9.003 9.003 0 019 18v-4.5m6 4.5c0 .733-.088 1.445-.253 2.128M9.75 16.5h4.5" />
                </svg>
                
                <!-- Heartbeat -->
                <svg v-else-if="getTimelineTheme(job.company).icon === 'heartbeat'" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" class="w-6 h-6">
                  <path stroke-linecap="round" stroke-linejoin="round" d="M21 8.25c0-2.485-2.099-4.5-4.688-4.5-1.935 0-3.597 1.126-4.312 2.733-.715-1.607-2.377-2.733-4.313-2.733C5.1 3.75 3 5.765 3 8.25c0 7.22 9 12 9 12s9-4.78 9-12z" />
                </svg>

                <!-- Rocket -->
                <svg v-else-if="getTimelineTheme(job.company).icon === 'rocket'" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" class="w-6 h-6">
                  <path stroke-linecap="round" stroke-linejoin="round" d="M15.59 14.37a6 6 0 01-5.84 7.38v-4.8m5.84-2.58a14.98 14.98 0 006.16-12.12A14.98 14.98 0 009.63 8.41a14.98 14.98 0 00-6.16 12.12c1.78-.17 3.52-.57 5.16-1.18M15.59 14.37a15.014 15.014 0 01-6.83 4.22m0 0L7.5 12h4.5m-4.5 4.8l-1.5-3.6" />
                </svg>

                <!-- Chart -->
                <svg v-else-if="getTimelineTheme(job.company).icon === 'chart'" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" class="w-6 h-6">
                  <path stroke-linecap="round" stroke-linejoin="round" d="M3 13.125C3 12.504 3.504 12 4.125 12h2.25c.621 0 1.125.504 1.125 1.125v6.75C7.5 20.496 6.996 21 6.375 21h-2.25A1.125 1.125 0 013 19.875v-6.75zM9.75 8.625c0-.621.504-1.125 1.125-1.125h2.25c.621 0 1.125.504 1.125 1.125v11.25c0 .621-.504 1.125-1.125 1.125h-2.25a1.125 1.125 0 01-1.125-1.125V8.625zM16.5 4.125c0-.621.504-1.125 1.125-1.125h2.25C20.496 3 21 3.504 21 4.125v15.75c0 .621-.504 1.125-1.125 1.125h-2.25a1.125 1.125 0 01-1.125-1.125V4.125z" />
                </svg>

                <!-- Microscope / Science -->
                <svg v-else xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" d="M6 18h12M12 18v3m0-6v-3m0 0a3 3 0 10-6 0v3m6-3h3.5a1.5 1.5 0 011.5 1.5V18M10 9l4 2.5M12 4.5a2.5 2.5 0 10-5 0v3h5v-3z" />
                </svg>
              </div>
            </div>
          </div>
        </div>
      </div>

      <div class="timeline-footer">
        <a href="#experience" class="btn btn-outline">
          <span>View Full Experience</span>
          <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" class="w-4 h-4">
            <path stroke-linecap="round" stroke-linejoin="round" d="M13.5 4.5L21 12m0 0l-7.5 7.5M21 12H3" />
          </svg>
        </a>
      </div>
    </div>
  </section>
</template>

<style scoped>
.timeline-section {
  padding: 80px 0;
  background-color: var(--bg-alt);
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

.timeline-container {
  position: relative;
  margin-bottom: 48px;
  padding-top: 32px;
}

.timeline-line {
  position: absolute;
  top: 32px;
  left: 0;
  right: 0;
  height: 2px;
  background-color: var(--border);
  z-index: 1;
}

.timeline-grid {
  display: grid;
  grid-template-columns: repeat(5, 1fr);
  gap: 24px;
  position: relative;
  z-index: 5;
}

.timeline-card-wrapper {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.timeline-node {
  width: 14px;
  height: 14px;
  border-radius: 50%;
  background-color: var(--bg-alt);
  border: 3px solid var(--accent-color);
  margin-bottom: 32px;
  z-index: 10;
  transition: transform 0.2s;
}

.timeline-card-wrapper:hover .node-dot {
  transform: scale(1.3);
}

.timeline-card {
  background: var(--bg-main);
  border: 1px solid var(--border);
  border-radius: var(--radius-md);
  padding: 24px;
  text-align: left;
  width: 100%;
  min-height: 250px;
  display: flex;
  flex-direction: column;
  position: relative;
  box-shadow: var(--shadow-sm);
  transition: var(--transition);
}

.timeline-card:hover {
  transform: translateY(-6px);
  box-shadow: var(--shadow-lg);
  border-color: var(--accent-color);
}

.period {
  font-family: var(--font-heading);
  font-size: 0.85rem;
  font-weight: 700;
  color: var(--accent-color);
  margin-bottom: 12px;
}

.company {
  font-size: 1.1rem;
  font-weight: 700;
  color: var(--navy);
  margin-bottom: 8px;
}

.role {
  font-size: 0.9rem;
  font-weight: 500;
  color: var(--text-primary);
  margin-bottom: 8px;
}

.domain {
  font-size: 0.85rem;
  color: var(--text-muted);
  margin-bottom: auto;
  line-height: 1.4;
}

.card-icon {
  width: 40px;
  height: 40px;
  border-radius: var(--radius-sm);
  display: flex;
  align-items: center;
  justify-content: center;
  margin-top: 16px;
}

.card-icon svg {
  width: 20px;
  height: 20px;
}

.timeline-footer {
  margin-top: 32px;
}

@media (max-width: 992px) {
  .timeline-line {
    display: none;
  }
  .timeline-grid {
    grid-template-columns: 1fr !important;
    gap: 32px;
  }
  .timeline-node {
    display: none;
  }
  .timeline-card {
    min-height: auto;
  }
}
</style>
