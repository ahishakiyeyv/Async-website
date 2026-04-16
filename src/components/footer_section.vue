<template>
  <footer class="footer">
    <div class="footer__content">
      <div class="footer__brand">
        <span class="footer__logo">Async Eng.</span>
        <p>Building the future, one line of code at a time.</p>
      </div>

      <div class="footer__links">
        <a href="#hero">Home</a>
        <a href="#about">About</a>
        <a href="#service">Services</a>
        <a href="#work">Work</a>
        <a href="#contact">Contact</a>
      </div>

      <div class="footer__social">
        <a href="#" aria-label="LinkedIn"><i class="fa fa-brands fa-linkedin-in"></i></a>
        <a href="#" aria-label="Twitter"><i class="fa fa-brands fa-twitter"></i></a>
        <a href="#" aria-label="GitHub"><i class="fa fa-brands fa-github"></i></a>
      </div>
    </div>

    <div class="footer__bottom">
      <p>&copy; 2026 Async Eng. All rights reserved.</p>
    </div>
  </footer>
</template>

<script setup></script>

<style scoped>
.footer {
  padding: 3rem 2rem 2rem;
  background: #020917;
  color: var(--color-text);
  border-top: 1px solid rgba(255, 255, 255, 0.08);
}

.footer__content {
  max-width: 1200px;
  margin: 0 auto;
  display: grid;
  grid-template-columns: 1fr auto 1fr;
  gap: 2rem;
  align-items: center;
  margin-bottom: 2rem;
}

.footer__brand {
  text-align: left;
}

.footer__logo {
  display: block;
  font-size: 1.5rem;
  font-weight: 700;
  color: var(--color-primary);
  margin-bottom: 0.5rem;
}

.footer__brand p {
  margin: 0;
  color: rgba(248, 249, 251, 0.6);
  font-size: 0.9rem;
}

.footer__links {
  display: flex;
  gap: 2rem;
  justify-content: center;
}

.footer__links a {
  color: rgba(248, 249, 251, 0.8);
  text-decoration: none;
  font-size: 0.95rem;
  transition: color 0.2s ease;
}

.footer__links a:hover {
  color: var(--color-primary);
}

.footer__social {
  display: flex;
  gap: 1rem;
  justify-content: flex-end;
}

.footer__social a {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  width: 2.5rem;
  height: 2.5rem;
  border-radius: 50%;
  background: rgba(1, 242, 255, 0.1);
  color: var(--color-primary);
  text-decoration: none;
  font-size: 0.9rem;
  font-weight: 600;
  transition: background 0.2s ease;
}

.footer__social a:hover {
  background: rgba(1, 242, 255, 0.2);
}

.footer__bottom {
  max-width: 1200px;
  margin: 0 auto;
  padding-top: 1rem;
  border-top: 1px solid rgba(255, 255, 255, 0.06);
  text-align: center;
}

.footer__bottom p {
  margin: 0;
  color: rgba(248, 249, 251, 0.5);
  font-size: 0.85rem;
}

@media (max-width: 768px) {
  .footer__content {
    grid-template-columns: 1fr;
    gap: 1.5rem;
    text-align: center;
  }

  .footer__links {
    justify-content: center;
    flex-wrap: wrap;
  }

  .footer__social {
    justify-content: center;
  }
}

@media (max-width: 480px) {
  .footer {
    padding: 2rem 1rem 1.5rem;
  }

  .footer__links {
    gap: 1rem;
  }

  .footer__links a {
    font-size: 0.9rem;
  }
}
</style>
