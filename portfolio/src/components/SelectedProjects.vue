<script setup lang="ts">
import projectsData from '../data/projects.json';
</script>

<template>
  <section id="projects" class="projects-section">
    <div class="container text-center">
      <h2 class="section-title">Selected Projects</h2>
      <p class="section-subtitle">A few highlights from my work across domains</p>
      
      <div class="projects-grid">
        <div 
          v-for="project in projectsData.projects" 
          :key="project.title" 
          class="project-card"
        >
          <!-- Custom SVG/Styled Logos based on project identifier -->
          <div class="logo-box">
            <!-- KRÜSS -->
            <div v-if="project.logo === 'kruss'" class="logo-kruss">
              <span class="kruss-text">KRÜSS</span>
              <div class="kruss-curve"></div>
            </div>

            <!-- HAUNI AREO -->
            <div v-else-if="project.logo === 'hauni'" class="logo-hauni">
              <svg viewBox="0 0 100 40" width="100" height="40" class="hauni-svg">
                <rect x="10" y="5" width="8" height="30" fill="#E11D48" />
                <rect x="24" y="5" width="8" height="15" fill="#E11D48" />
                <rect x="24" y="25" width="8" height="10" fill="#E11D48" />
                <rect x="38" y="5" width="8" height="30" fill="#E11D48" />
                <rect x="52" y="5" width="14" height="30" rx="3" fill="#E11D48" />
                <rect x="72" y="5" width="8" height="30" fill="#E11D48" />
              </svg>
            </div>

            <!-- SOTAX -->
            <div v-else-if="project.logo === 'sotax'" class="logo-sotax">
              <span class="sotax-text">SOTAX</span>
            </div>

            <!-- Medgen Solutions -->
            <div v-else-if="project.logo === 'medgen'" class="logo-medgen">
              <svg viewBox="0 0 100 40" width="100" height="40" class="medgen-svg">
                <circle cx="25" cy="20" r="12" fill="none" stroke="#0D9488" stroke-width="3" />
                <circle cx="35" cy="20" r="12" fill="none" stroke="#2563EB" stroke-width="3" opacity="0.8" />
                <text x="54" y="25" font-family="Outfit" font-size="14" font-weight="700" fill="#0F172A">Medgen</text>
              </svg>
            </div>

            <!-- DDS -->
            <div v-else-if="project.logo === 'dds'" class="logo-dds">
              <div class="dds-badge">DDS</div>
            </div>

            <!-- Blue Penguin -->
            <div v-else-if="project.logo === 'bluepenguin'" class="logo-penguin">
              <svg viewBox="0 0 100 40" width="100" height="40" class="penguin-svg">
                <!-- Cute Penguin SVG -->
                <ellipse cx="25" cy="20" rx="12" ry="15" fill="#0F172A" />
                <ellipse cx="25" cy="22" rx="8" ry="11" fill="#FFFFFF" />
                <circle cx="21" cy="15" r="2" fill="#0F172A" />
                <circle cx="29" cy="15" r="2" fill="#0F172A" />
                <polygon points="23,17 27,17 25,20" fill="#F97316" />
                <text x="44" y="25" font-family="Outfit" font-size="12" font-weight="700" fill="#0F172A">Blue Penguin</text>
              </svg>
            </div>
          </div>
          
          <h3 class="project-title">{{ project.title }}</h3>
          <p class="project-domain">{{ project.domain }}</p>
          
          <a href="#projects" class="project-link">
            <span>View Details</span>
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2.5" stroke="currentColor" class="w-4 h-4">
              <path stroke-linecap="round" stroke-linejoin="round" d="M13.5 4.5L21 12m0 0l-7.5 7.5M21 12H3" />
            </svg>
          </a>
        </div>
      </div>

      <div class="projects-footer">
        <a href="#projects" class="btn btn-outline">
          <span>View All Projects</span>
          <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" class="w-4 h-4">
            <path stroke-linecap="round" stroke-linejoin="round" d="M13.5 4.5L21 12m0 0l-7.5 7.5M21 12H3" />
          </svg>
        </a>
      </div>
    </div>
  </section>
</template>

<style scoped>
.projects-section {
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

.projects-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 24px;
  margin-bottom: 48px;
}

.project-card {
  background: var(--bg-main);
  border: 1px solid var(--border);
  border-radius: var(--radius-lg);
  padding: 36px 24px;
  text-align: left;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  transition: var(--transition);
  box-shadow: var(--shadow-sm);
}

.project-card:hover {
  transform: translateY(-6px);
  box-shadow: var(--shadow-lg);
  border-color: var(--primary);
}

.logo-box {
  height: 60px;
  display: flex;
  align-items: center;
  margin-bottom: 24px;
  width: 100%;
}

/* KRÜSS Logo */
.logo-kruss {
  display: flex;
  flex-direction: column;
  position: relative;
}

.kruss-text {
  font-family: var(--font-heading);
  font-size: 1.6rem;
  font-weight: 800;
  color: #1e3a8a;
  letter-spacing: -0.05em;
  line-height: 1;
}

.kruss-curve {
  height: 3px;
  width: 80%;
  background: linear-gradient(90deg, #1e3a8a 0%, #3b82f6 100%);
  border-radius: 2px;
  margin-top: 4px;
}

/* SOTAX Logo */
.logo-sotax {
  font-family: var(--font-heading);
  font-size: 1.5rem;
  font-weight: 800;
  color: #2563eb;
  letter-spacing: 0.1em;
}

/* DDS Logo */
.logo-dds {
  background-color: #2563eb;
  color: #ffffff;
  font-family: var(--font-heading);
  font-size: 1.5rem;
  font-weight: 800;
  padding: 4px 16px;
  border-radius: 4px;
}

.project-title {
  font-size: 1.25rem;
  font-weight: 700;
  color: var(--navy);
  margin-bottom: 8px;
  font-family: var(--font-heading);
}

.project-domain {
  font-size: 0.9rem;
  color: var(--text-secondary);
  margin-bottom: 24px;
  line-height: 1.4;
  min-height: 40px;
}

.project-link {
  display: inline-flex;
  align-items: center;
  gap: 6px;
  color: var(--primary);
  font-family: var(--font-heading);
  font-weight: 600;
  font-size: 0.9rem;
  text-decoration: none;
  transition: var(--transition);
}

.project-card:hover .project-link {
  color: var(--primary-hover);
}

.project-link svg {
  transition: transform 0.2s;
}

.project-link:hover svg {
  transform: translateX(4px);
}

.projects-footer {
  margin-top: 32px;
}

@media (max-width: 992px) {
  .projects-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 576px) {
  .projects-grid {
    grid-template-columns: 1fr;
  }
}
</style>
