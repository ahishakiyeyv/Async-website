<template>
  <section class="section1">
    <div class="hero-section">
      <div class="hero-span">Engineering the Future - Asynchronously</div>
      <h1>We Build What <span>Tomorrow</span> Demands</h1>
      <p>
        A collective of engineers crafting intelligent software, scalable platforms, and sustainable
        energy solutions on our own terms.
      </p>
      <div class="btn-group">
        <a href="#services" class="btn-primary">See Our Work</a>
        <a href="#contact" class="btn-secondary">Explore Services</a>
      </div>
    </div>
  </section>
</template>
<style scoped>
.section1 {
  background-image: url('../src/assets/images/bg-hero.jpeg');
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
}
.hero-section {
  display: flex;
  align-items: center;
  flex-direction: column;
  color: var(--color-text);
  text-align: center;
  padding: 8rem 20rem;
  background-color: rgba(2, 9, 23, 0.8);
}
.hero-span {
  font-size: 0.9rem;
  font-weight: 500;
  letter-spacing: 0.1em;
  color: var(--color-secondary);
  background-color: rgba(2, 9, 23, 0.8);
  margin-bottom: 1rem;
  border: 0.3px solid rgba(1, 242, 255, 0.2);
  border-radius: 1rem;
  padding: 0.5rem 1rem;
}
.hero-section h1 {
  font-size: 4rem;
  font-weight: 600;
  margin-bottom: 1rem;
  letter-spacing: 5px;
}
.hero-section h1 span {
  color: var(--color-primary);
  background: linear-gradient(to bottom, #63cad6 0%, #3a8ca3 100%);
  background-clip: text;
  -webkit-text-fill-color: transparent;
  filter: drop-shadow(0 0 15px rgba(99, 202, 214, 0.4));
  letter-spacing: 0.2rem;
}
.hero-section p {
  font-size: 1.2rem;
  color: var(--color-muted);
  margin-bottom: 2rem;
  text-align: center;
  line-height: 1.5rem;
  width: 70%;
}
.btn-group {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 1rem;
}
.btn-primary {
  background-color: var(--color-primary);
  color: var(--color-background);
  border: none;
  border-radius: 0.5rem;
  padding: 0.75rem 1.5rem;
  font-size: 1.1rem;
  font-weight: 500;
  text-decoration: none;
  cursor: pointer;
  transition: all 0.3s ease-in-out;
}
.btn-primary:hover {
  background-color: var(--color-secondary);
}
.btn-secondary {
  background-color: transparent;
  color: var(--color-text);
  border: 1px solid var(--color-text);
  border-radius: 0.5rem;
  padding: 0.75rem 1.5rem;
  font-size: 1.1rem;
  text-decoration: none;
  font-weight: 500;
  cursor: pointer;
  transition: all 0.3s ease-in-out;
}
.btn-secondary:hover {
  background-color: var(--color-secondary);
  border-color: var(--color-secondary);
}

@media (max-width: 1100px) {
  .hero-section {
    padding: 6rem 10rem;
  }

  .hero-section h1 {
    font-size: 3.5rem;
  }

  .hero-section p {
    font-size: 1.1rem;
    width: 80%;
  }
}

@media (max-width: 760px) {
  .hero-section {
    padding: 5rem 3rem;
  }

  .hero-span {
    font-size: 0.85rem;
    padding: 0.4rem 0.8rem;
  }

  .hero-section h1 {
    font-size: 2.8rem;
    letter-spacing: 3px;
  }

  .hero-section p {
    font-size: 1rem;
    width: 90%;
    line-height: 1.6rem;
  }

  .btn-group {
    flex-direction: column;
    gap: 0.75rem;
  }

  .btn-primary,
  .btn-secondary {
    width: 100%;
    max-width: 300px;
  }
}

@media (max-width: 480px) {
  .hero-section {
    padding: 4rem 1.5rem;
  }

  .hero-span {
    font-size: 0.8rem;
    padding: 0.35rem 0.7rem;
    margin-bottom: 0.75rem;
  }

  .hero-section h1 {
    font-size: 2.2rem;
    letter-spacing: 2px;
  }

  .hero-section p {
    font-size: 0.95rem;
    width: 100%;
    line-height: 1.5rem;
    margin-bottom: 1.5rem;
  }

  .btn-primary,
  .btn-secondary {
    padding: 0.7rem 1.2rem;
    font-size: 1rem;
  }
}
</style>
