<template>
  <section class="service-section" id="services">
    <div class="service-section__intro">
      <span class="service-section__eyebrow">What We Do</span>
      <h2 class="service-section__title">Services That <span>Scale</span></h2>
    </div>

    <div class="service-section__cards">
      <article class="service-card">
        <div class="service-card__icon" aria-hidden="true">
          <i class="fa fa-solid fa-brain"></i>
        </div>
        <h3>AI Solutions</h3>
        <p>
          Machine learning models, NLP systems, computer vision, and intelligent automation tailored
          to your business.
        </p>
      </article>

      <article class="service-card">
        <div class="service-card__icon" aria-hidden="true">
          <svg
            viewBox="0 0 24 24"
            fill="none"
            stroke="currentColor"
            stroke-width="1.8"
            stroke-linecap="round"
            stroke-linejoin="round"
          >
            <rect x="6" y="4" width="12" height="16" rx="2" />
            <path d="M12 18h.01" />
          </svg>
        </div>
        <h3>Mobile Development</h3>
        <p>Native and cross-platform apps with fluid experiences on iOS and Android.</p>
      </article>

      <article class="service-card">
        <div class="service-card__icon" aria-hidden="true">
          <i class="fa fa-solid fa-globe"></i>
        </div>
        <h3>Web Development</h3>
        <p>
          High-performance web apps, progressive web experiences, and scalable cloud architectures.
        </p>
      </article>

      <article class="service-card">
        <div class="service-card__icon" aria-hidden="true">
          <i class="fa fa-solid fa-bolt"></i>
        </div>
        <h3>Energy Engineering</h3>
        <p>
          Smart grid solutions, renewable energy systems, and IoT-powered energy management
          platforms.
        </p>
      </article>

      <article class="service-card">
        <div class="service-card__icon" aria-hidden="true">
          <i class="fa fa-solid fa-palette"></i>
        </div>
        <h3>UI/UX Design</h3>
        <p>
          Research-driven design systems, prototyping, and interfaces that users genuinely love.
        </p>
      </article>

      <article class="service-card">
        <div class="service-card__icon" aria-hidden="true">
          <i class="fa fa-solid fa-grip"></i>
        </div>
        <h3>Custom Software</h3>
        <p>
          End-to-end engineering for complex systems — from architecture to deployment and beyond.
        </p>
      </article>
    </div>
  </section>
</template>

<script setup></script>

<style scoped>
.service-section {
  padding: 5rem 2rem 3rem;
  background:
    radial-gradient(circle at top, rgba(1, 242, 255, 0.08) 0%, transparent 30%),
    linear-gradient(180deg, #020917 0%, #05070d 100%);
  color: var(--color-text);
}

.service-section__intro {
  max-width: 750px;
  margin: 0 auto 2.5rem;
  text-align: center;
}

.service-section__eyebrow {
  display: inline-flex;
  margin-bottom: 1rem;
  padding: 0.75rem 1.5rem;
  border-radius: 999px;
  font-size: 0.78rem;
  letter-spacing: 0.2em;
  text-transform: uppercase;
  color: var(--color-primary);
  border: 1px solid rgba(1, 242, 255, 0.2);
  background: rgba(1, 242, 255, 0.05);
}

.service-section__title {
  margin: 0;
  font-size: 3rem;
  font-weight: 700;
  letter-spacing: 0.3rem;
  line-height: 1.02;
}

.service-section__title span {
  color: var(--color-secondary);
  background: linear-gradient(to bottom, #63cad6 0%, #3a8ca3 100%);
  background-clip: text;
  -webkit-text-fill-color: transparent;
  filter: drop-shadow(0 0 15px rgba(99, 202, 214, 0.4));
  letter-spacing: 0.2rem;
}

.service-section__cards {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 1.5rem;
  max-width: 1240px;
  margin: 0 auto;
}

.service-card {
  background: rgba(12, 18, 30, 0.86);
  border: 1px solid rgba(255, 255, 255, 0.06);
  border-radius: 1.75rem;
  padding: 2rem;
  min-height: 260px;
  box-shadow: 0 22px 60px rgba(0, 0, 0, 0.16);
  transition:
    transform 0.3s ease,
    border-color 0.3s ease,
    background 0.3s ease;
  display: flex;
  flex-direction: column;
  gap: 1.2rem;
}

.service-card:hover {
  transform: translateY(-4px);
  border-color: rgba(1, 242, 255, 0.18);
  background: rgba(13, 21, 36, 0.96);
}

.service-card__icon {
  width: 3rem;
  height: 3rem;
  display: grid;
  place-items: center;
  border-radius: 1rem;
  color: var(--color-primary);
  background: rgba(1, 242, 255, 0.1);
}

.service-card__icon svg {
  width: 1.4rem;
  height: 1.4rem;
}

.service-card h3 {
  margin: 0;
  font-size: 1.1rem;
  color: var(--color-text);
}

.service-card p {
  margin: 0;
  color: var(--color-muted);
  line-height: 1.8;
}

@media (max-width: 1100px) {
  .service-section {
    padding: 4.5rem 1.5rem 2.25rem;
  }

  .service-section__cards {
    grid-template-columns: repeat(2, minmax(0, 1fr));
  }
}

@media (max-width: 760px) {
  .service-section {
    padding: 3.5rem 1.2rem 2rem;
  }

  .service-section__intro {
    margin-bottom: 2rem;
  }

  .service-card {
    min-height: auto;
    padding: 1.75rem;
  }

  .service-section__cards {
    grid-template-columns: 1fr;
  }
}

@media (max-width: 480px) {
  .service-section {
    padding: 2.8rem 1rem 1.5rem;
  }

  .service-section__eyebrow {
    padding: 0.6rem 1.2rem;
    font-size: 0.72rem;
  }

  .service-section__title {
    font-size: 2rem;
  }

  .service-card {
    padding: 1.4rem;
  }

  .service-card h3 {
    font-size: 1rem;
  }
}
</style>
