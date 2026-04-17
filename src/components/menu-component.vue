<template>
  <header class="menu-bar">
    <div class="menu-bar__brand">Async Eng.</div>
    <nav class="menu-bar__nav">
      <a href="#about">About</a>
      <a href="#services">Services</a>
      <a href="#portfolio">Portfolio</a>
      <a href="#contact">Contact</a>
    </nav>
    <a class="menu-bar__cta" href="#contact">Get in Touch</a>

    <!-- Hamburger Menu Button -->
    <button class="menu-bar__hamburger" @click="toggleMenu" :class="{ 'is-active': isMenuOpen }">
      <span class="hamburger-line"></span>
      <span class="hamburger-line"></span>
      <span class="hamburger-line"></span>
    </button>

    <!-- Mobile Menu Backdrop -->
    <div
      class="mobile-menu-backdrop"
      :class="{ 'is-visible': isMenuOpen }"
      @click="closeMenu"
    ></div>

    <!-- Mobile Menu Overlay -->
    <div class="mobile-menu" :class="{ 'is-open': isMenuOpen }">
      <div class="mobile-menu__content">
        <button class="mobile-menu__close" @click="toggleMenu">
          <svg
            width="24"
            height="24"
            viewBox="0 0 24 24"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              d="M18 6L6 18"
              stroke="currentColor"
              stroke-width="2"
              stroke-linecap="round"
              stroke-linejoin="round"
            />
            <path
              d="M6 6L18 18"
              stroke="currentColor"
              stroke-width="2"
              stroke-linecap="round"
              stroke-linejoin="round"
            />
          </svg>
        </button>
        <nav class="mobile-menu__nav">
          <a href="#services" @click="closeMenu">Services</a>
          <a href="#portfolio" @click="closeMenu">Portfolio</a>
          <a href="#about" @click="closeMenu">About</a>
          <a href="#contact" @click="closeMenu">Contact</a>
        </nav>
        <a class="mobile-menu__cta" href="#contact" @click="closeMenu">Get in Touch</a>
      </div>
    </div>
  </header>
</template>

<script setup>
import { ref, watch } from 'vue'

const isMenuOpen = ref(false)

const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value
}

const closeMenu = () => {
  isMenuOpen.value = false
}

// Prevent body scroll when mobile menu is open
watch(isMenuOpen, (newValue) => {
  if (newValue) {
    document.body.style.overflow = 'hidden'
  } else {
    document.body.style.overflow = ''
  }
})
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
  z-index: 200;
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

/* Hamburger Menu Styles */
.menu-bar__hamburger {
  display: none;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  width: 40px;
  height: 40px;
  background: none;
  border: none;
  cursor: pointer;
  padding: 0;
  z-index: 201;
}

.hamburger-line {
  width: 18px;
  height: 2px;
  background: #ffffff;
  margin: 3px 0;
  transition: all 0.3s ease;
  transform-origin: center;
}

.menu-bar__hamburger.is-active .hamburger-line:nth-child(1) {
  transform: rotate(45deg) translate(5px, 5px);
}

.menu-bar__hamburger.is-active .hamburger-line:nth-child(2) {
  opacity: 0;
}

.menu-bar__hamburger.is-active .hamburger-line:nth-child(3) {
  transform: rotate(-45deg) translate(7px, -6px);
}

/* Mobile Menu Backdrop */
.mobile-menu-backdrop {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0);
  z-index: 999;
  opacity: 0;
  visibility: hidden;
  transition:
    opacity 0.3s ease,
    background 0.3s ease,
    visibility 0.3s ease;
  pointer-events: none;
}

.mobile-menu-backdrop.is-visible {
  background: rgba(0, 0, 0, 0.5);
  opacity: 1;
  visibility: visible;
  pointer-events: auto;
}

/* Mobile Menu Overlay */
.mobile-menu {
  position: fixed;
  top: 0;
  right: 0;
  width: 280px;
  height: 100vh;
  background: rgba(10, 10, 13, 0.95);
  backdrop-filter: blur(20px);
  z-index: 1001;
  border-left: 1px solid rgba(255, 255, 255, 0.08);
  overflow-y: auto;
  overflow-x: hidden;
  transform: translateX(100%);
  display: none;
  transition: transform 0.3s cubic-bezier(0.4, 0, 0.2, 1);
  will-change: transform;
  -webkit-overflow-scrolling: touch;
}

.mobile-menu.is-open {
  transform: translateX(0);
  display: block;
}

.mobile-menu__content {
  padding: 1.2rem 1rem;
  height: 100%;
  display: flex;
  flex-direction: column;
}

.mobile-menu__close {
  align-self: flex-end;
  display: flex;
  align-items: center;
  justify-content: center;
  width: 44px;
  height: 44px;
  background: none;
  border: none;
  color: #ffffff;
  cursor: pointer;
  padding: 0;
  margin-bottom: 1.5rem;
  border-radius: 8px;
  transition: background 0.2s ease;
}

.mobile-menu__close:hover {
  background: rgba(255, 255, 255, 0.1);
}

.mobile-menu__nav {
  display: flex;
  flex-direction: column;
  gap: 1rem;
  margin-bottom: 1.5rem;
}

.mobile-menu__nav a {
  color: #71879c;
  text-decoration: none;
  font-size: 1rem;
  font-weight: 500;
  padding: 0.8rem 0.9rem;
  border-bottom: 1px solid rgba(255, 255, 255, 0.08);
  border-radius: 0.5rem;
  transition:
    color 0.2s ease,
    background 0.2s ease;
  display: block;
}

.mobile-menu__nav a:hover {
  color: #ffffff;
}

.mobile-menu__cta {
  margin-top: auto;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 1rem 1.5rem;
  border-radius: 12px;
  background: #01f2ff;
  color: #020917;
  text-decoration: none;
  font-weight: 600;
  font-size: 0.95rem;
  text-align: center;
  min-height: 44px;
  box-shadow: 0 15px 30px rgba(1, 242, 255, 0.15);
  transition:
    transform 0.2s ease,
    box-shadow 0.2s ease;
}

.mobile-menu__cta:hover {
  transform: translateY(-1px);
  box-shadow: 0 18px 32px rgba(1, 242, 255, 0.22);
}

@media (max-width: 1100px) {
  .menu-bar {
    gap: 60px;
    padding: 1rem 1.5rem;
  }

  .menu-bar__nav {
    gap: 1.8rem;
  }
}

@media (max-width: 760px) {
  .menu-bar {
    gap: 30px;
    padding: 0.9rem 1.2rem;
  }

  .menu-bar__brand {
    font-size: 1rem;
    flex-shrink: 0;
  }

  .menu-bar__nav {
    gap: 1.2rem;
  }

  .menu-bar__nav a {
    font-size: 0.875rem;
  }

  .menu-bar__cta {
    padding: 0.75rem 1.2rem;
    font-size: 0.8rem;
    flex-shrink: 0;
  }
}

@media (max-width: 480px) {
  .menu-bar {
    justify-content: space-between;
    gap: 0;
    padding: 0.65rem 0.75rem;
    min-height: 52px;
  }

  .menu-bar__brand {
    font-size: 0.85rem;
    flex-shrink: 0;
  }

  .menu-bar__nav {
    display: none;
  }

  .menu-bar__cta {
    display: none;
  }

  .menu-bar__hamburger {
    display: flex;
    width: 44px;
    height: 44px;
    margin-left: auto;
  }

  .hamburger-line {
    width: 16px;
    height: 1.5px;
    margin: 3px 0;
  }

  .mobile-menu {
    width: 280px;
  }

  .mobile-menu__content {
    padding: 1rem 0.9rem;
  }

  .mobile-menu__close {
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 0.5rem;
    margin-bottom: 1.2rem;
    width: 44px;
    height: 44px;
  }

  .mobile-menu__close svg {
    width: 20px;
    height: 20px;
  }

  .mobile-menu__nav {
    gap: 0.4rem;
    margin-bottom: 1.2rem;
  }

  .mobile-menu__nav a {
    font-size: 0.9rem;
    padding: 0.7rem 0.8rem;
    border-radius: 0.5rem;
    transition:
      background 0.2s ease,
      color 0.2s ease;
  }

  .mobile-menu__nav a:active,
  .mobile-menu__nav a:hover {
    background: rgba(1, 242, 255, 0.08);
    color: #ffffff;
  }

  .mobile-menu__cta {
    width: 100%;
    padding: 0.85rem 1.2rem;
    font-size: 0.9rem;
  }
}

@media (max-width: 360px) {
  .menu-bar {
    padding: 0.6rem 0.65rem;
  }

  .menu-bar__brand {
    font-size: 0.8rem;
  }

  .menu-bar__hamburger {
    width: 44px;
    height: 44px;
  }

  .hamburger-line {
    width: 14px;
    height: 1.5px;
    margin: 3px 0;
  }

  .mobile-menu {
    width: 260px;
  }

  .mobile-menu__content {
    padding: 0.9rem 0.8rem;
  }

  .mobile-menu__close {
    width: 44px;
    height: 44px;
    margin-bottom: 1rem;
  }

  .mobile-menu__nav {
    gap: 0.3rem;
    margin-bottom: 1rem;
  }

  .mobile-menu__nav a {
    font-size: 0.85rem;
    padding: 0.6rem 0.7rem;
  }

  .mobile-menu__cta {
    padding: 0.8rem 1rem;
    font-size: 0.85rem;
  }
}
</style>
