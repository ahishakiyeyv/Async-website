<template>
  <header class="menu-bar">
    <div class="menu-bar__brand">Async Eng.</div>
    <nav class="menu-bar__nav">
      <a href="#services">Services</a>
      <a href="#portfolio">Portfolio</a>
      <a href="#about">About</a>
      <a href="#contact">Contact</a>
    </nav>
    <a class="menu-bar__cta" href="#contact">Get in Touch</a>
  </header>
</template>

<script setup>
</script>

<style scoped>
.menu-bar {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 80px;
  padding: 1rem 2rem;
  background: #0a0a0d;
  backdrop-filter: blur(4px);
  position: sticky;
  top: 0;
  z-index: 20;
  border-bottom: 1px solid rgba(255, 255, 255, 0.08);
}

.menu-bar__brand {
  font-size: 1.1rem;
  font-weight: 700;
  letter-spacing: 0.08em;
  color: #54f0ff;
}

.menu-bar__nav {
  display: flex;
  align-items: center;
  gap: 2rem;
  flex: 1;
  justify-content: flex-end;
}

.menu-bar__nav a {
  color: #71879c;
  text-decoration: none;
  font-size: 0.95rem;
  transition: color 0.2s ease;
}

.menu-bar__nav a:hover {
  color: #ffffff;
}

.menu-bar__cta {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  padding: 0.85rem 1.4rem;
  border-radius: 15px;
  background: #01f2ff;
  color: #020917;
  text-decoration: none;
  font-weight: 600;
  font-size: 0.9rem;
  box-shadow: 0 15px 30px rgba(1, 242, 255, 0.15);
  transition:
    transform 0.2s ease,
    box-shadow 0.2s ease;
}

.menu-bar__cta:hover {
  transform: translateY(-1px);
  box-shadow: 0 18px 32px rgba(1, 242, 255, 0.22);
}

@media (max-width: 768px) {
  .menu-bar {
    flex-wrap: wrap;
    justify-content: center;
    text-align: center;
  }

  .menu-bar__nav {
    width: 100%;
    justify-content: center;
    gap: 1rem;
    margin-top: 0.75rem;
    flex-wrap: wrap;
  }

  .menu-bar__cta {
    width: 100%;
    max-width: 320px;
    margin-top: 0.75rem;
  }
}
</style>
