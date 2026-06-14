<script setup lang="ts">
// Call To Action - Presentational
</script>

<template>
  <section id="contact" class="cta-section">
    <div class="container">
      <div class="cta-box">
        <div class="cta-left">
          <div class="chat-icon">
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-8 h-8">
              <path stroke-linecap="round" stroke-linejoin="round" d="M8.625 9.75a.625.625 0 11-1.25 0 .625.625 0 011.25 0zm4.5 0a.625.625 0 11-1.25 0 .625.625 0 011.25 0zm4.5 0a.625.625 0 11-1.25 0 .625.625 0 011.25 0z" />
              <path stroke-linecap="round" stroke-linejoin="round" d="M8.625 12a.375.375 0 11-.75 0 .375.375 0 01.75 0zm4.5 0a.375.375 0 11-.75 0 .375.375 0 01.75 0zm4.5 0a.375.375 0 11-.75 0 .375.375 0 01.75 0z" />
              <path stroke-linecap="round" stroke-linejoin="round" d="M2.25 12c0-5.385 4.365-9.75 9.75-9.75s9.75 4.365 9.75 9.75-4.365 9.75-9.75 9.75a9.753 9.753 0 01-5.021-1.39l-4.256 1.135a.75.75 0 01-.94-1.012l1.135-4.256A9.753 9.753 0 012.25 12z" />
            </svg>
          </div>
          <div class="cta-text">
            <h3 class="cta-title">Let's build something great together</h3>
            <p class="cta-desc">I'm always open to discussing interesting projects, collaborations or opportunities.</p>
          </div>
        </div>
        
        <div class="cta-right">
          <a href="mailto:anuviswan@gmail.com" class="btn btn-primary cta-btn">
            <span>Let's Connect</span>
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2.5" stroke="currentColor" class="w-4 h-4">
              <path stroke-linecap="round" stroke-linejoin="round" d="M13.5 4.5L21 12m0 0l-7.5 7.5M21 12H3" />
            </svg>
          </a>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.cta-section {
  padding: 60px 0;
  background-color: var(--bg-alt);
  border-bottom: 1px solid var(--border);
}

.cta-box {
  background-color: var(--bg-main);
  border: 1px solid var(--border);
  border-radius: var(--radius-lg);
  padding: 40px 48px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 32px;
  box-shadow: var(--shadow-md);
}

.cta-left {
  display: flex;
  align-items: center;
  gap: 24px;
  text-align: left;
}

.chat-icon {
  width: 56px;
  height: 56px;
  background-color: var(--primary-light);
  color: var(--primary);
  border-radius: var(--radius-md);
  display: flex;
  align-items: center;
  justify-content: center;
  flex-shrink: 0;
}

.cta-title {
  font-size: 1.4rem;
  font-weight: 700;
  color: var(--navy);
  margin-bottom: 6px;
}

.cta-desc {
  font-size: 0.95rem;
  color: var(--text-secondary);
}

.cta-btn {
  white-space: nowrap;
}

@media (max-width: 768px) {
  .cta-box {
    flex-direction: column;
    padding: 32px 24px;
    text-align: center;
  }
  
  .cta-left {
    flex-direction: column;
    align-items: center;
    text-align: center;
  }
  
  .cta-right {
    width: 100%;
  }
  
  .cta-btn {
    width: 100%;
  }
}
</style>
