<script setup lang="ts">
const linkedin = import.meta.env.VITE_LINKEDIN || '';
const github = import.meta.env.VITE_GITHUB || '';
const csharpcorner = import.meta.env.VITE_CSHARPCORNER || '';
const bytelanguage = import.meta.env.VITE_BYTELANGUAGE || '';

const getHref = (url: string) => {
  if (!url) return '#';
  if (url.startsWith('http://') || url.startsWith('https://')) {
    return url;
  }
  return `https://${url}`;
};
</script>

<template>
  <section id="presence" class="presence-section">
    <div class="container">
      <div class="presence-box">
        <h2 class="presence-title">Professional Presence</h2>
        
        <div class="presence-grid">
          <!-- LinkedIn -->
          <a :href="getHref(linkedin)" target="_blank" rel="noopener noreferrer" class="presence-card">
            <div class="card-icon linkedin">
              <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor">
                <path d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.762 0 5-2.239 5-5v-14c0-2.761-2.238-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.779-1.75-1.75s.784-1.75 1.75-1.75 1.75.779 1.75 1.75-.784 1.75-1.75 1.75zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.396-2.586 7-2.777 7 2.476v6.759z"/>
              </svg>
            </div>
            <div class="card-info">
              <span class="presence-name">LinkedIn</span>
              <span class="presence-desc">Connect professionally</span>
            </div>
            <svg class="arrow-icon" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" d="M4.5 19.5l15-15m0 0H8.25m11.25 0v11.25" />
            </svg>
          </a>

          <!-- GitHub -->
          <a :href="getHref(github)" target="_blank" rel="noopener noreferrer" class="presence-card">
            <div class="card-icon github">
              <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor">
                <path fill-rule="evenodd" clip-rule="evenodd" d="M12 2C6.477 2 2 6.477 2 12c0 4.42 2.865 8.166 6.839 9.489.5.092.682-.217.682-.482 0-.237-.008-.866-.013-1.7-2.782.603-3.369-1.34-3.369-1.34-.454-1.156-1.11-1.464-1.11-1.464-.908-.62.069-.608.069-.608 1.003.07 1.531 1.03 1.531 1.03.892 1.529 2.341 1.087 2.91.832.092-.647.35-1.088.636-1.338-2.22-.253-4.555-1.11-4.555-4.943 0-1.091.39-1.984 1.029-2.683-.103-.253-.446-1.27.098-2.647 0 0 .84-.269 2.75 1.025A9.564 9.564 0 0112 6.844c.85.004 1.705.115 2.504.337 1.909-1.294 2.747-1.025 2.747-1.025.546 1.377.203 2.394.1 2.647.64.699 1.028 1.592 1.028 2.683 0 3.842-2.339 4.687-4.566 4.935.359.309.678.919.678 1.852 0 1.336-.012 2.415-.012 2.743 0 .267.18.579.688.481C19.138 20.161 22 16.416 22 12c0-5.523-4.477-10-10-10z" />
              </svg>
            </div>
            <div class="card-info">
              <span class="presence-name">GitHub</span>
              <span class="presence-desc">Projects & experiments</span>
            </div>
            <svg class="arrow-icon" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" d="M4.5 19.5l15-15m0 0H8.25m11.25 0v11.25" />
            </svg>
          </a>

          <!-- ByteLanguage -->
          <a :href="getHref(bytelanguage)" target="_blank" rel="noopener noreferrer" class="presence-card">
            <div class="card-icon bytelanguage">
              <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2.2" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" d="M19.5 14.25v-2.625a3.375 3.375 0 00-3.375-3.375h-1.5A1.125 1.125 0 0113.5 7.125v-1.5A3.375 3.375 0 0010.125 2.25H6.75A2.25 2.25 0 004.5 4.5v15a2.25 2.25 0 002.25 2.25h10.5a2.25 2.25 0 002.25-2.25v-5.25z" />
                <path stroke-linecap="round" stroke-linejoin="round" d="M8.25 15h7.5M8.25 11.25h7.5m-7.5-3.75h3" />
              </svg>
            </div>
            <div class="card-info">
              <span class="presence-name">ByteLanguage</span>
              <span class="presence-desc">Technical articles & blog</span>
            </div>
            <svg class="arrow-icon" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" d="M4.5 19.5l15-15m0 0H8.25m11.25 0v11.25" />
            </svg>
          </a>

          <!-- C# Corner -->
          <a :href="getHref(csharpcorner)" target="_blank" rel="noopener noreferrer" class="presence-card">
            <div class="card-icon csharp">
              <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor">
                <rect width="24" height="24" rx="4" fill="#007acc"/>
                <text x="12" y="16" font-family="monospace" font-size="12" font-weight="900" fill="#ffffff" text-anchor="middle">C#</text>
              </svg>
            </div>
            <div class="card-info">
              <span class="presence-name">C# Corner</span>
              <span class="presence-desc">MVP articles & publications</span>
            </div>
            <svg class="arrow-icon" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" d="M4.5 19.5l15-15m0 0H8.25m11.25 0v11.25" />
            </svg>
          </a>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.presence-section {
  padding: 32px 0;
  background-color: var(--bg-main);
}

.presence-box {
  border: 1px solid var(--border);
  border-radius: var(--radius-lg);
  padding: 32px 40px;
  background: var(--bg-alt);
}

.presence-title {
  font-size: 1.15rem;
  font-weight: 700;
  color: var(--text-secondary);
  margin-bottom: 24px;
  font-family: var(--font-heading);
}

.presence-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 32px;
}

.presence-card {
  display: flex;
  align-items: center;
  gap: 16px;
  text-decoration: none;
  position: relative;
  padding-right: 24px;
  transition: var(--transition);
}

.presence-card::after {
  content: '';
  position: absolute;
  right: -16px;
  top: 10%;
  height: 80%;
  width: 1px;
  background-color: var(--border);
}

.presence-grid > *:last-child::after {
  display: none;
}

.card-icon {
  width: 48px;
  height: 48px;
  border-radius: var(--radius-sm);
  display: flex;
  align-items: center;
  justify-content: center;
  flex-shrink: 0;
}

.card-icon.linkedin {
  background-color: #eff6ff;
  color: #0077b5;
}

.card-icon.github {
  background-color: #f8fafc;
  color: #0f172a;
}

.card-icon.bytelanguage {
  background-color: #eff6ff;
  color: #2563eb;
}

.card-icon svg {
  width: 28px;
  height: 28px;
}

.card-info {
  display: flex;
  flex-direction: column;
}

.presence-name {
  font-family: var(--font-heading);
  font-weight: 700;
  font-size: 1rem;
  color: var(--navy);
  margin-bottom: 2px;
}

.presence-desc {
  font-size: 0.8rem;
  color: var(--text-muted);
}

.arrow-icon {
  width: 16px;
  height: 16px;
  color: var(--text-muted);
  opacity: 0;
  transition: var(--transition);
  position: absolute;
  right: 0;
  top: 50%;
  transform: translateY(-50%);
}

.presence-card:hover {
  transform: translateY(-2px);
}

.presence-card:hover .presence-name {
  color: var(--primary);
}

.presence-card:hover .arrow-icon {
  opacity: 1;
  color: var(--primary);
}

@media (max-width: 992px) {
  .presence-grid {
    grid-template-columns: repeat(2, 1fr);
    gap: 24px;
  }
  .presence-card::after {
    display: none;
  }
}

@media (max-width: 576px) {
  .presence-grid {
    grid-template-columns: 1fr;
    gap: 24px;
  }
}
</style>
