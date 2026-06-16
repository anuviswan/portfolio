<script setup lang="ts">
const showDownloadResume = import.meta.env.VITE_SHOW_DOWNLOAD_RESUME !== 'false';
</script>

<template>
  <header class="header">
    <div class="container nav-wrapper">
      <div class="logo-area">
        <div class="logo-badge">AV</div>
        <div class="logo-text">
          <span class="logo-name">Anu Viswan</span>
          <span class="logo-title">Lead Software Architect /  Principal Engineer</span>
        </div>
      </div>
      
      <nav class="nav-menu">
        <a href="#home" class="nav-link active">Home</a>
      </nav>

      <a v-if="showDownloadResume" href="/resume.pdf" download class="btn btn-outline download-btn">
        <span>Download Resume</span>
        <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2" class="icon">
          <path stroke-linecap="round" stroke-linejoin="round" d="M4 16v1a3 3 0 003 3h10a3 3 0 003-3v-1m-4-4l-4 4m0 0l-4-4m4 4V4" />
        </svg>
      </a>
    </div>
  </header>
</template>

<style scoped>
.header {
  border-bottom: 1px solid var(--border);
  background: var(--bg-main);
  position: sticky;
  top: 0;
  z-index: 50;
  backdrop-filter: blur(8px);
  background: rgba(255, 255, 255, 0.9);
}

.nav-wrapper {
  display: flex;
  align-items: center;
  justify-content: space-between;
  height: 80px;
}

.logo-area {
  display: flex;
  align-items: center;
  gap: 12px;
  cursor: pointer;
}

.logo-badge {
  background-color: var(--primary-light);
  color: var(--primary);
  font-family: var(--font-heading);
  font-size: 1.4rem;
  font-weight: 700;
  width: 44px;
  height: 44px;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 50%;
  border: 2px solid var(--primary);
}

.logo-text {
  display: flex;
  flex-direction: column;
  line-height: 1.2;
}

.logo-name {
  font-weight: 700;
  font-size: 1.15rem;
  color: var(--navy);
  font-family: var(--font-heading);
}

.logo-title {
  font-size: 0.8rem;
  color: var(--text-muted);
}

.nav-menu {
  display: flex;
  gap: 32px;
}

.nav-link {
  text-decoration: none;
  color: var(--text-secondary);
  font-family: var(--font-heading);
  font-weight: 500;
  font-size: 0.95rem;
  transition: var(--transition);
  position: relative;
  padding: 8px 0;
}

.nav-link:hover, .nav-link.active {
  color: var(--primary);
}

.nav-link.active::after {
  content: '';
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  height: 2px;
  background-color: var(--primary);
  border-radius: 2px;
}

.download-btn {
  padding: 10px 18px;
  font-size: 0.9rem;
}

.icon {
  width: 16px;
  height: 16px;
}

@media (max-width: 768px) {
  .nav-menu {
    display: none; /* Hide on mobile for simplicity or can wrap to burger */
  }
}
</style>
