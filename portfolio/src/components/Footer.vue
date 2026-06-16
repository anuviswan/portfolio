<script setup lang="ts">
const scrollToTop = () => {
  window.scrollTo({
    top: 0,
    behavior: 'smooth'
  });
};

const email = import.meta.env.VITE_EMAIL || '';
const linkedin = import.meta.env.VITE_LINKEDIN || '';
const github = import.meta.env.VITE_GITHUB || '';
const csharpcorner = import.meta.env.VITE_CSHARPCORNER || '';

const cleanUrlForDisplay = (url: string) => {
  if (!url) return '';
  return url.replace(/^(https?:\/\/)?(www\.)?/, '');
};

const getHref = (url: string) => {
  if (!url) return '#';
  if (url.startsWith('http://') || url.startsWith('https://')) {
    return url;
  }
  return `https://${url}`;
};
</script>

<template>
  <footer class="footer">
    <div class="container footer-wrapper">
      <div class="footer-center">
        <p class="copyright">© 2026 Anu Viswan. All rights reserved.</p>
      </div>

      <div class="footer-right">
        <button @click="scrollToTop" class="back-to-top" aria-label="Scroll to top">
          <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2.5" stroke="currentColor" class="w-5 h-5">
            <path stroke-linecap="round" stroke-linejoin="round" d="M4.5 15.75l7.5-7.5 7.5 7.5" />
          </svg>
        </button>
      </div>
    </div>
  </footer>
</template>

<style scoped>
.footer {
  border-top: 1px solid var(--border);
  padding: 40px 0;
  background-color: var(--bg-main);
}

.footer-wrapper {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 24px;
}

.copyright {
  font-size: 0.9rem;
  color: var(--text-muted);
}

.footer-center {
  display: flex;
  align-items: center;
  gap: 32px;
}

.social-link {
  display: flex;
  align-items: center;
  gap: 8px;
  text-decoration: none;
  color: var(--text-secondary);
  font-size: 0.9rem;
  transition: var(--transition);
}

.social-link svg {
  width: 20px;
  height: 20px;
  flex-shrink: 0;
  transition: var(--transition);
}

.social-link:hover {
  color: var(--primary);
}

.social-link:hover svg {
  transform: translateY(-1px);
}

.back-to-top {
  width: 40px;
  height: 40px;
  border-radius: 50%;
  border: 1px solid var(--border);
  background-color: var(--bg-main);
  color: var(--text-secondary);
  display: flex;
  align-items: center;
  justify-content: center;
  cursor: pointer;
  transition: var(--transition);
}

.back-to-top svg {
  width: 20px;
  height: 20px;
}

.back-to-top:hover {
  background-color: var(--primary-light);
  border-color: var(--primary);
  color: var(--primary);
  transform: translateY(-2px);
}

@media (max-width: 992px) {
  .footer-wrapper {
    flex-direction: column-reverse;
    text-align: center;
  }
  
  .footer-center {
    flex-direction: column;
    gap: 16px;
  }
}
</style>
