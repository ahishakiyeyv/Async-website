<template>
  <section class="about-section" id="about">
    <div class="about-section__content">
      <span class="about-section__eyebrow">Who We Are</span>
      <h2 class="about-section__title">
        A Collective of <span>Builders</span><br />Who Refuse to Wait
      </h2>
      <p class="about-section__copy">
        Async Eng. was born when a group of passionate engineers decided to stop waiting for
        permission and start building the future. From AI platforms to energy systems, we work
        across disciplines because real innovation doesn't respect boundaries.
      </p>
    </div>

    <div class="about-section__grid">
      <article class="about-card">
        <div class="about-card__icon" aria-hidden="true">
          <svg
            viewBox="0 0 24 24"
            fill="none"
            stroke="currentColor"
            stroke-width="1.8"
            stroke-linecap="round"
            stroke-linejoin="round"
          >
            <path d="M20 21v-2a4 4 0 0 0-4-4H8a4 4 0 0 0-4 4v2" />
            <circle cx="12" cy="7" r="4" />
          </svg>
        </div>
        <div class="about-card__value">30+</div>
        <div class="about-card__label">Engineers</div>
      </article>

      <article class="about-card">
        <div class="about-card__icon" aria-hidden="true">
          <i class="fa fa-solid fa-rocket"></i>
        </div>
        <div class="about-card__value">80+</div>
        <div class="about-card__label">Projects Delivered</div>
      </article>

      <article class="about-card">
        <div class="about-card__icon" aria-hidden="true">
          <i class="fa fa-solid fa-globe"></i>
        </div>
        <div class="about-card__value">15+</div>
        <div class="about-card__label">Countries Served</div>
      </article>

      <article class="about-card">
        <div class="about-card__icon" aria-hidden="true">
          <i class="fa fa-solid fa-medal"></i>
        </div>
        <div class="about-card__value">5+</div>
        <div class="about-card__label">Years of Innovation</div>
      </article>
    </div>

    <div class="about-section__feature-grid">
      <article class="about-feature-card">
        <div class="about-feature-card__icon" aria-hidden="true">
          <i class="fa fa-solid fa-code"></i>
        </div>
        <div>
          <h3>Code-First Culture</h3>
          <p>Every solution starts with clean, scalable architecture built to operate at speed.</p>
        </div>
      </article>

      <article class="about-feature-card">
        <div class="about-feature-card__icon" aria-hidden="true">
          <i class="fa fa-solid fa-microchip"></i>
        </div>
        <div>
          <h3>AI-Native Thinking</h3>
          <p>We embed intelligence into everything we build so systems learn, adapt, and scale.</p>
        </div>
      </article>

      <article class="about-feature-card">
        <div class="about-feature-card__icon" aria-hidden="true">
          <i class="fa fa-solid fa-bolt"></i>
        </div>
        <div>
          <h3>Relentless Velocity</h3>
          <p>Ship fast, iterate smarter, and keep momentum without cutting corners.</p>
        </div>
      </article>
    </div>
  </section>
</template>

<script setup></script>

<style scoped>
.about-section {
  padding: 5rem 2rem 3rem;
  background:
    radial-gradient(circle at 50% 50%, rgba(1, 242, 255, 0.08) 0%, transparent 35%),
    linear-gradient(180deg, rgba(2, 9, 23, 0.98) 0%, #020917 100%);
  color: var(--color-text);
}

.about-section__content {
  max-width: 900px;
  margin: 0 auto 3rem;
  text-align: center;
}

.about-section__eyebrow {
  display: inline-block;
  margin-bottom: 1rem;
  padding: 0.7rem 1.3rem;
  border-radius: 999px;
  font-size: 0.85rem;
  letter-spacing: 0.18em;
  text-transform: uppercase;
  color: var(--color-primary);
  border: 1px solid rgba(1, 242, 255, 0.2);
  background: rgba(1, 242, 255, 0.05);
}

.about-section__title {
  margin: 0;
  font-size: 3rem;
  line-height: 1.02;
  letter-spacing: 0.3rem;
  font-weight: 700;
}

.about-section__title span {
  color: var(--color-secondary);
  background: linear-gradient(to bottom, #63cad6 0%, #3a8ca3 100%);
  background-clip: text;
  -webkit-text-fill-color: transparent;
  filter: drop-shadow(0 0 15px rgba(99, 202, 214, 0.4));
  letter-spacing: 0.2rem;
}

.about-section__copy {
  max-width: 760px;
  margin: 1.7rem auto 0;
  font-size: 1.1rem;
  line-height: 1.85;
  color: var(--color-muted);
}

.about-section__grid {
  display: grid;
  grid-template-columns: repeat(4, minmax(0, 1fr));
  gap: 1.25rem;
  max-width: 1180px;
  margin: 0 auto;
}

.about-section__feature-grid {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 1.25rem;
  max-width: 1180px;
  margin: 5rem auto 0;
}

.about-feature-card {
  background: rgba(8, 12, 20, 0.85);
  border: 1px solid rgba(255, 255, 255, 0.08);
  border-radius: 1.5rem;
  padding: 2rem;
  display: grid;
  grid-template-columns: auto 1fr;
  gap: 1.25rem;
  align-items: start;
  box-shadow: 0 22px 55px rgba(0, 0, 0, 0.22);
  transition:
    transform 0.28s ease,
    border-color 0.28s ease,
    background 0.28s ease;
}

.about-feature-card:hover {
  transform: translateY(-3px);
  background: rgba(12, 18, 32, 0.95);
  border-color: rgba(1, 242, 255, 0.16);
}

.about-feature-card__icon {
  width: 3rem;
  height: 3rem;
  display: grid;
  place-items: center;
  border-radius: 1rem;
  background: rgba(1, 242, 255, 0.08);
  color: var(--color-primary);
}

.about-feature-card__icon svg {
  width: 1.4rem;
  height: 1.4rem;
}

.about-feature-card h3 {
  margin: 0;
  font-size: 1.15rem;
  color: var(--color-text);
  font-weight: 400;
}

.about-feature-card p {
  margin: 0.5rem 0 0;
  color: var(--color-muted);
  line-height: 1.8;
}

.about-card {
  background: rgba(10, 16, 29, 0.82);
  border: 1px solid rgba(255, 255, 255, 0.06);
  border-radius: 1.5rem;
  padding: 1rem;
  min-height: 180px;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  justify-content: center;
  gap: 1rem;
  box-shadow: 0 24px 60px rgba(0, 0, 0, 0.24);
  transition:
    transform 0.3s ease,
    border-color 0.3s ease;
}

.about-card:hover {
  transform: translateY(-4px);
  border-color: rgba(1, 242, 255, 0.18);
}

.about-card__icon {
  width: 3rem;
  height: 3rem;
  display: grid;
  place-items: center;
  border-radius: 1rem;
  background: rgba(1, 242, 255, 0.1);
  color: var(--color-primary);
}

.about-card__icon svg {
  width: 1.4rem;
  height: 1.4rem;
}

.about-card__value {
  margin: 0;
  font-size: 2.75rem;
  font-weight: 300;
  color: var(--color-secondary);
}

.about-card__label {
  text-transform: uppercase;
  letter-spacing: 0.2em;
  font-size: 0.72rem;
  color: rgba(248, 249, 251, 0.7);
}

@media (max-width: 1100px) {
  .about-section {
    padding: 4.5rem 1.5rem 2.5rem;
  }

  .about-section__grid,
  .about-section__feature-grid {
    grid-template-columns: repeat(2, minmax(0, 1fr));
  }
}

@media (max-width: 720px) {
  .about-section {
    padding: 3.5rem 1.25rem 2rem;
  }

  .about-section__content {
    margin-bottom: 2rem;
  }

  .about-section__title {
    font-size: 2.3rem;
  }

  .about-section__copy {
    font-size: 0.98rem;
    line-height: 1.9;
  }

  .about-section__grid {
    grid-template-columns: 1fr;
  }

  .about-card {
    min-height: auto;
    padding: 1.75rem;
  }
}

@media (max-width: 480px) {
  .about-section {
    padding: 2.75rem 1rem 1.5rem;
  }

  .about-section__eyebrow {
    font-size: 0.75rem;
    padding: 0.6rem 1.1rem;
  }

  .about-section__title {
    font-size: 1.95rem;
  }

  .about-card {
    padding: 1.5rem;
  }

  .about-card__value {
    font-size: 2.1rem;
  }
}
</style>
