<template>
  <section class="contact-section" id="contact">
    <div class="contact-section__content">
      <span class="contact-section__eyebrow">Get in touch</span>
      <h2 class="contact-section__title">Let’s Build <span>Together</span></h2>
      <p class="contact-section__subtitle">
        Have a project in mind? We’d love to hear about it. Drop us a line and let’s explore how we
        can bring your vision to life.
      </p>

      <div class="contact-card">
        <form class="contact-form" action="#" method="post">
          <div class="contact-form__row contact-form__row--split">
            <label class="contact-field">
              <span>Your Name</span>
              <input type="text" placeholder="Your Name" />
            </label>
            <label class="contact-field">
              <span>Your Email</span>
              <input type="email" placeholder="Your Email" />
            </label>
          </div>

          <label class="contact-field">
            <span>Subject</span>
            <input type="text" placeholder="Subject" />
          </label>

          <label class="contact-field contact-field--full">
            <span>Tell us about your project...</span>
            <textarea rows="6" placeholder="Tell us about your project..."></textarea>
          </label>

          <div class="contact-form__action">
            <button type="submit" class="contact-form__button">
              Send Message
              <svg
                width="18"
                height="18"
                viewBox="0 0 24 24"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path d="M5 12H19" stroke="currentColor" stroke-width="2" stroke-linecap="round" />
                <path
                  d="M13 6L19 12L13 18"
                  stroke="currentColor"
                  stroke-width="2"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                />
              </svg>
            </button>
          </div>

          <div class="contact-card__footer">
            <div class="contact-card__item">
              <span class="contact-card__icon" aria-hidden="true"
                ><i class="fa fa-regular fa-envelope"></i
              ></span>
              <a href="mailto:hello@asynceng.com">hello@asynceng.com</a>
            </div>
            <div class="contact-card__item">
              <span class="contact-card__icon" aria-hidden="true"
                ><i class="fa fa-solid fa-map-pin"></i
              ></span>
              <p>Remote-first, Worldwide</p>
            </div>
          </div>
        </form>
      </div>
    </div>
  </section>
</template>

<script setup></script>

<style scoped>
.contact-section {
  padding: 5rem 2rem 4rem;
  background:
    radial-gradient(circle at 30% 50%, rgba(1, 242, 255, 0.08) 0%, transparent 32%),
    linear-gradient(180deg, #020917 0%, #05070d 100%);
  color: var(--color-text);
}

.contact-section__content {
  max-width: 1120px;
  margin: 0 auto;
  text-align: center;
}

.contact-section__eyebrow {
  display: inline-flex;
  margin-bottom: 1rem;
  padding: 0.75rem 1.5rem;
  border-radius: 999px;
  text-transform: uppercase;
  letter-spacing: 0.18em;
  font-size: 0.78rem;
  color: var(--color-primary);
  border: 1px solid rgba(1, 242, 255, 0.25);
  background: rgba(1, 242, 255, 0.06);
}

.contact-section__title {
  margin: 0;
  font-size: 3rem;
  letter-spacing: 0.3rem;
  line-height: 1.02;
  font-weight: 700;
}

.contact-section__title span {
  color: var(--color-secondary);
  background: linear-gradient(to bottom, #63cad6 0%, #3a8ca3 100%);
  background-clip: text;
  -webkit-text-fill-color: transparent;
  filter: drop-shadow(0 0 15px rgba(99, 202, 214, 0.4));
  letter-spacing: 0.2rem;
}

.contact-section__subtitle {
  max-width: 720px;
  margin: 1.25rem auto 0;
  font-size: 1rem;
  line-height: 1.85;
  color: var(--color-muted);
}

.contact-card {
  margin: 3rem auto 0;
  padding: 2rem 2rem;
  width: 100%;
  max-width: 920px;
  border-radius: 2rem;
  background: rgba(255, 255, 255, 0.04);
  border: 1px solid rgba(255, 255, 255, 0.08);
  box-shadow: 0 30px 70px rgba(0, 0, 0, 0.25);
  backdrop-filter: blur(18px);
}

.contact-form {
  display: grid;
  gap: 1rem;
  width: 100%;
}

.contact-form__row {
  display: grid;
  gap: 2rem;
  width: 100%;
}

.contact-form__row--split {
  grid-template-columns: repeat(2, minmax(0, 1fr));
}

.contact-field {
  display: grid;
  gap: 0.75rem;
  text-align: left;
  font-size: 0.95rem;
  color: rgba(248, 249, 251, 0.84);
}

.contact-field span {
  font-weight: 600;
}

.contact-field input,
.contact-field textarea {
  width: 100%;
  min-height: 1.2rem;
  padding: 1rem 1.1rem;
  border-radius: 1rem;
  border: 1px solid rgba(255, 255, 255, 0.12);
  background: rgba(7, 14, 26, 0.9);
  color: var(--color-text);
  font-size: 1rem;
  outline: none;
  box-sizing: border-box;
}

.contact-field textarea {
  min-height: 180px;
  resize: vertical;
}

.contact-field input::placeholder,
.contact-field textarea::placeholder {
  color: rgba(248, 249, 251, 0.4);
}

.contact-form__action {
  display: flex;
  justify-content: center;
}

.contact-form__button {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  gap: 0.75rem;
  padding: 1rem 2rem;
  border-radius: 15px;
  border: 1px solid var(--color-primary);
  background: rgba(1, 242, 255, 0.12);
  color: var(--color-primary);
  font-size: 1rem;
  font-weight: 500;
  cursor: pointer;
  transition:
    transform 0.2s ease,
    background 0.2s ease,
    box-shadow 0.2s ease;
}

.contact-form__button:hover {
  transform: translateY(-2px);
  background: rgba(1, 242, 255, 0.18);
  box-shadow: 0 18px 30px rgba(1, 242, 255, 0.12);
}

.contact-card__footer {
  margin-top: 1rem;
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 3rem;
}

.contact-card__item {
  display: flex;
  align-items: center;
  gap: 1rem;
}

.contact-card__icon {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  color: var(--color-primary);
  font-size: 1.2rem;
}

.contact-card__footer a,
.contact-card__footer p {
  margin: 0;
  color: var(--color-text);
  font-size: 0.7rem;
  font-weight: 100;
  letter-spacing: 0.2rem;
}

.contact-card__footer a {
  color: var(--color-primary);
  text-decoration: none;
}

@media (max-width: 1100px) {
  .contact-section {
    padding: 4.5rem 1.5rem 3.5rem;
  }

  .contact-card {
    padding: 1.8rem;
  }

  .contact-form__row--split {
    grid-template-columns: 1fr;
  }
}

@media (max-width: 760px) {
  .contact-section {
    padding: 3.5rem 1.2rem 3rem;
  }

  .contact-section__title {
    font-size: 2.8rem;
  }

  .contact-section__subtitle {
    font-size: 0.98rem;
  }

  .contact-card {
    margin: 2.5rem 0 0;
    padding: 1.6rem;
  }

  .contact-form__button {
    width: 100%;
  }

  .contact-card__footer {
    grid-template-columns: 1fr;
  }
}

@media (max-width: 480px) {
  .contact-section {
    padding: 2.8rem 1rem 2.5rem;
  }

  .contact-section__eyebrow {
    padding: 0.65rem 1.1rem;
    font-size: 0.72rem;
  }

  .contact-section__title {
    font-size: 2.2rem;
  }

  .contact-card {
    padding: 1.25rem;
    border-radius: 1.5rem;
  }

  .contact-field input,
  .contact-field textarea {
    padding: 0.95rem 1rem;
  }

  .contact-card__item {
    padding: 1rem;
  }
}
</style>
