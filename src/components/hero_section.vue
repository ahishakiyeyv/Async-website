<template>
  <section class="section1">
    <div class="hero-bg">
      <div class="glow glow-1"></div>
      <div class="glow glow-2"></div>
      <div class="glow glow-3"></div>
      <div class="particles">
        <span v-for="n in 20" :key="n" class="particle" :style="{ '--i': n }"></span>
      </div>
    </div>
    <div class="hero-container">
      <div class="hero-left">
        <div class="badge-wrapper">
          <span class="badge">
            <span class="badge-ring"></span>
            Engineering the Future
          </span>
        </div>
        <h1 class="hero-heading">
          <span class="line">We Build What</span>
          <span class="line highlight-text">
            <span class="highlight-inner">Tomorrow</span>
            <span class="highlight-glow"></span>
          </span>
          <span class="line">Demands</span>
        </h1>
        <p class="hero-text">
          A collective of visionary engineers crafting intelligent software, scalable platforms, and
          sustainable energy solutions that shape the future on our own terms.
        </p>
        <div class="cta-wrapper">
          <a href="#services" class="btn-main">
            <span>See Our Work</span>
            <svg
              class="arrow"
              viewBox="0 0 24 24"
              fill="none"
              stroke="currentColor"
              stroke-width="2"
            >
              <path d="M5 12h14M12 5l7 7-7 7" />
            </svg>
          </a>
          <a href="#contact" class="btn-outline">
            <span>Explore Services</span>
          </a>
        </div>
        <div class="trust-badges">
          <div class="trust-item">
            <span class="trust-num">150+</span>
            <span class="trust-label">Projects</span>
          </div>
          <div class="trust-item">
            <span class="trust-num">50+</span>
            <span class="trust-label">Clients</span>
          </div>
          <div class="trust-item">
            <span class="trust-num">99%</span>
            <span class="trust-label">Success</span>
          </div>
        </div>
      </div>
      <div class="hero-right">
        <div class="visual-card main-card">
          <div class="card-glow"></div>
          <div class="card-content">
            <div class="code-block">
              <div class="code-header">
                <span class="dot"></span>
                <span class="dot"></span>
                <span class="dot"></span>
              </div>
              <pre
                class="code-body"
              ><code><span class="kwd">const</span> <span class="var">future</span> = <span class="str">"async"</span>;
<span class="kwd">const</span> <span class="var">build</span> = <span class="fn">createTomorrow</span>();
<span class="kwd">await</span> <span class="fn">innovate</span>(<span class="var">dreams</span>);
<span class="cmt">// Future is now</span></code></pre>
            </div>
          </div>
        </div>
        <div class="float-tag tag-1">
          <span class="tag-icon">⚡</span>
          <span class="tag-text">Fast</span>
        </div>
        <div class="float-tag tag-2">
          <span class="tag-icon">🔐</span>
          <span class="tag-text">Secure</span>
        </div>
        <div class="float-tag tag-3">
          <span class="tag-icon">📈</span>
          <span class="tag-text">Scale</span>
        </div>
      </div>
    </div>
  </section>
</template>
<style scoped>
.section1 {
  position: relative;
  min-height: 100vh;
  background: #020917;
  overflow: hidden;
}

.hero-bg {
  position: absolute;
  inset: 0;
  pointer-events: none;
}

.glow {
  position: absolute;
  border-radius: 50%;
  filter: blur(100px);
}

.glow-1 {
  width: 800px;
  height: 800px;
  background: radial-gradient(circle, rgba(1, 242, 255, 0.15) 0%, transparent 60%);
  top: -300px;
  right: -200px;
  animation: drift 15s ease-in-out infinite;
}

.glow-2 {
  width: 600px;
  height: 600px;
  background: radial-gradient(circle, rgba(99, 202, 214, 0.12) 0%, transparent 60%);
  bottom: -200px;
  left: -100px;
  animation: drift 20s ease-in-out infinite reverse;
}

.glow-3 {
  width: 400px;
  height: 400px;
  background: radial-gradient(circle, rgba(58, 140, 163, 0.1) 0%, transparent 60%);
  top: 40%;
  left: 30%;
  animation: pulse-glow 8s ease-in-out infinite;
}

@keyframes drift {
  0%,
  100% {
    transform: translate(0, 0) scale(1);
  }
  33% {
    transform: translate(40px, -30px) scale(1.05);
  }
  66% {
    transform: translate(-20px, 20px) scale(0.95);
  }
}

@keyframes pulse-glow {
  0%,
  100% {
    opacity: 0.5;
    transform: scale(1);
  }
  50% {
    opacity: 0.8;
    transform: scale(1.1);
  }
}

.particles {
  position: absolute;
  inset: 0;
}

.particle {
  position: absolute;
  width: 4px;
  height: 4px;
  background: rgba(1, 242, 255, 0.4);
  border-radius: 50%;
  animation: twinkle 4s ease-in-out infinite;
  animation-delay: calc(var(--i) * 0.2s);
}

.particle:nth-child(odd) {
  background: rgba(99, 202, 214, 0.3);
}

.particle:nth-child(1) {
  top: 10%;
  left: 15%;
}
.particle:nth-child(2) {
  top: 20%;
  left: 80%;
}
.particle:nth-child(3) {
  top: 35%;
  left: 25%;
}
.particle:nth-child(4) {
  top: 45%;
  left: 70%;
}
.particle:nth-child(5) {
  top: 55%;
  left: 40%;
}
.particle:nth-child(6) {
  top: 65%;
  left: 85%;
}
.particle:nth-child(7) {
  top: 75%;
  left: 20%;
}
.particle:nth-child(8) {
  top: 85%;
  left: 60%;
}
.particle:nth-child(9) {
  top: 15%;
  left: 50%;
}
.particle:nth-child(10) {
  top: 60%;
  left: 10%;
}
.particle:nth-child(11) {
  top: 30%;
  left: 90%;
}
.particle:nth-child(12) {
  top: 80%;
  left: 35%;
}
.particle:nth-child(13) {
  top: 5%;
  left: 65%;
}
.particle:nth-child(14) {
  top: 90%;
  left: 75%;
}
.particle:nth-child(15) {
  top: 40%;
  left: 5%;
}
.particle:nth-child(16) {
  top: 25%;
  left: 45%;
}
.particle:nth-child(17) {
  top: 70%;
  left: 55%;
}
.particle:nth-child(18) {
  top: 50%;
  left: 95%;
}
.particle:nth-child(19) {
  top: 5%;
  left: 30%;
}
.particle:nth-child(20) {
  top: 95%;
  left: 45%;
}

@keyframes twinkle {
  0%,
  100% {
    opacity: 0.2;
    transform: scale(1);
  }
  50% {
    opacity: 0.8;
    transform: scale(1.5);
  }
}

.hero-container {
  position: relative;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 6rem;
  max-width: 1400px;
  margin: 0 auto;
  padding: 7rem 5%;
  z-index: 1;
}

.hero-left {
  flex: 1;
  max-width: 600px;
}

.badge-wrapper {
  margin-bottom: 2rem;
}

.badge {
  display: inline-flex;
  align-items: center;
  gap: 0.75rem;
  background: rgba(1, 242, 255, 0.08);
  border: 1px solid rgba(1, 242, 255, 0.15);
  border-radius: 3rem;
  padding: 0.6rem 1.2rem;
  font-size: 0.8rem;
  font-weight: 500;
  color: var(--color-secondary);
  letter-spacing: 0.08em;
  text-transform: uppercase;
}

.badge-ring {
  width: 8px;
  height: 8px;
  background: var(--color-secondary);
  border-radius: 50%;
  box-shadow: 0 0 10px var(--color-secondary);
  animation: blink 2s ease-in-out infinite;
}

@keyframes blink {
  0%,
  100% {
    opacity: 1;
  }
  50% {
    opacity: 0.4;
  }
}

.hero-heading {
  font-size: 4.2rem;
  font-weight: 700;
  line-height: 1.15;
  margin-bottom: 1.5rem;
  color: var(--color-text);
}

.hero-heading .line {
  display: block;
}

.highlight-text {
  position: relative;
  display: inline-block;
}

.highlight-inner {
  background: linear-gradient(135deg, #01f2ff 0%, #63cad6 40%, #3a8ca3 100%);
  -webkit-background-clip: text;
  background-clip: text;
  -webkit-text-fill-color: transparent;
}

.highlight-glow {
  position: absolute;
  bottom: -5px;
  left: 0;
  width: 100%;
  height: 30px;
  background: linear-gradient(90deg, transparent, rgba(1, 242, 255, 0.3), transparent);
  filter: blur(15px);
}

.hero-text {
  font-size: 1.15rem;
  color: var(--color-muted);
  line-height: 1.75;
  margin-bottom: 2.5rem;
}

.cta-wrapper {
  display: flex;
  gap: 1.25rem;
  margin-bottom: 3rem;
}

.btn-main {
  display: inline-flex;
  align-items: center;
  gap: 0.6rem;
  background: linear-gradient(135deg, #01f2ff 0%, #63cad6 100%);
  color: #020917;
  border: none;
  border-radius: 0.6rem;
  padding: 0.95rem 1.8rem;
  font-size: 0.95rem;
  font-weight: 600;
  text-decoration: none;
  cursor: pointer;
  transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
  box-shadow: 0 4px 20px rgba(1, 242, 255, 0.25);
}

.btn-main:hover {
  transform: translateY(-3px);
  box-shadow: 0 8px 30px rgba(1, 242, 255, 0.4);
}

.btn-main .arrow {
  width: 18px;
  height: 18px;
  transition: transform 0.3s ease;
}

.btn-main:hover .arrow {
  transform: translateX(4px);
}

.btn-outline {
  display: inline-flex;
  align-items: center;
  background: transparent;
  color: var(--color-text);
  border: 1px solid rgba(255, 255, 255, 0.15);
  border-radius: 0.6rem;
  padding: 0.95rem 1.8rem;
  font-size: 0.95rem;
  font-weight: 500;
  text-decoration: none;
  cursor: pointer;
  transition: all 0.3s ease;
}

.btn-outline:hover {
  background: rgba(255, 255, 255, 0.03);
  border-color: var(--color-secondary);
}

.trust-badges {
  display: flex;
  gap: 2.5rem;
}

.trust-item {
  display: flex;
  flex-direction: column;
}

.trust-num {
  font-size: 1.8rem;
  font-weight: 700;
  color: var(--color-secondary);
}

.trust-label {
  font-size: 0.75rem;
  color: var(--color-muted);
  text-transform: uppercase;
  letter-spacing: 0.05em;
}

.hero-right {
  position: relative;
  flex: 1;
  display: flex;
  justify-content: center;
  align-items: center;
  max-width: 500px;
}

.visual-card {
  position: relative;
  background: rgba(10, 22, 40, 0.6);
  border: 1px solid rgba(99, 202, 214, 0.15);
  border-radius: 1.2rem;
  padding: 1.8rem;
  width: 100%;
  backdrop-filter: blur(10px);
}

.card-glow {
  position: absolute;
  inset: -1px;
  border-radius: 1.2rem;
  background: linear-gradient(135deg, rgba(1, 242, 255, 0.1), transparent, rgba(99, 202, 214, 0.1));
  z-index: -1;
  filter: blur(20px);
}

.code-block {
  background: rgba(2, 9, 23, 0.8);
  border-radius: 0.8rem;
  overflow: hidden;
}

.code-header {
  display: flex;
  gap: 0.5rem;
  padding: 0.8rem 1rem;
  background: rgba(99, 202, 214, 0.05);
  border-bottom: 1px solid rgba(99, 202, 214, 0.1);
}

.code-header .dot {
  width: 10px;
  height: 10px;
  border-radius: 50%;
}

.code-header .dot:nth-child(1) {
  background: #ff5f57;
}
.code-header .dot:nth-child(2) {
  background: #febc2e;
}
.code-header .dot:nth-child(3) {
  background: #28c840;
}

.code-body {
  margin: 0;
  padding: 1.2rem;
  font-family: 'Fira Code', 'Consolas', monospace;
  font-size: 0.85rem;
  line-height: 1.7;
  color: var(--color-muted);
}

.code-body .kwd {
  color: #c792ea;
}
.code-body .var {
  color: #82aaff;
}
.code-body .str {
  color: #c3e88d;
}
.code-body .fn {
  color: #82aaff;
}
.code-body .cmt {
  color: #546e7a;
  font-style: italic;
}

.float-tag {
  position: absolute;
  display: flex;
  align-items: center;
  gap: 0.5rem;
  background: rgba(10, 22, 40, 0.85);
  border: 1px solid rgba(99, 202, 214, 0.2);
  border-radius: 0.6rem;
  padding: 0.6rem 0.9rem;
  font-size: 0.8rem;
  color: var(--color-text);
  box-shadow: 0 8px 25px rgba(0, 0, 0, 0.2);
  animation: float-elem 5s ease-in-out infinite;
}

.tag-icon {
  font-size: 1rem;
}

.tag-1 {
  top: 5%;
  right: -10px;
  animation-delay: 0s;
}

.tag-2 {
  bottom: 35%;
  left: -25px;
  animation-delay: 1.5s;
}

.tag-3 {
  bottom: 8%;
  right: 15%;
  animation-delay: 3s;
}

@keyframes float-elem {
  0%,
  100% {
    transform: translateY(0);
  }
  50% {
    transform: translateY(-12px);
  }
}

@media (max-width: 1100px) {
  .hero-container {
    flex-direction: column;
    text-align: center;
    padding: 5rem 5%;
    gap: 4rem;
  }

  .hero-left {
    max-width: 100%;
  }

  .hero-heading {
    font-size: 3rem;
  }

  .cta-wrapper {
    justify-content: center;
  }

  .trust-badges {
    justify-content: center;
  }

  .hero-right {
    width: 100%;
    max-width: 450px;
  }

  .float-tag {
    display: none;
  }
}

@media (max-width: 640px) {
  .hero-heading {
    font-size: 2.2rem;
  }

  .hero-text {
    font-size: 1rem;
  }

  .cta-wrapper {
    flex-direction: column;
    gap: 0.8rem;
  }

  .btn-main,
  .btn-outline {
    width: 100%;
    justify-content: center;
  }

  .trust-badges {
    flex-direction: column;
    gap: 1.2rem;
    align-items: center;
  }
}

/* Additional Enhanced CSS */
.section1::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 1px;
  background: linear-gradient(90deg, transparent, rgba(1, 242, 255, 0.3), transparent);
}

.hero-bg::after {
  content: '';
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  height: 150px;
  background: linear-gradient(to top, rgba(2, 9, 23, 0.8), transparent);
  pointer-events: none;
}

.badge {
  transition: all 0.3s ease;
}

.badge:hover {
  background: rgba(1, 242, 255, 0.12);
  border-color: rgba(1, 242, 255, 0.3);
  transform: scale(1.02);
}

.hero-heading {
  animation: fadeInUp 0.8s ease-out;
}

@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(30px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.hero-text {
  animation: fadeInUp 0.8s ease-out 0.2s both;
}

.cta-wrapper {
  animation: fadeInUp 0.8s ease-out 0.4s both;
}

.trust-badges {
  animation: fadeInUp 0.8s ease-out 0.6s both;
}

.visual-card {
  animation: fadeInRight 1s ease-out 0.3s both;
}

@keyframes fadeInRight {
  from {
    opacity: 0;
    transform: translateX(40px);
  }
  to {
    opacity: 1;
    transform: translateX(0);
  }
}

.code-block {
  transition: all 0.3s ease;
}

.code-block:hover {
  box-shadow: 0 0 30px rgba(1, 242, 255, 0.1);
}

.float-tag {
  transition: all 0.3s ease;
}

.float-tag:hover {
  transform: translateY(-5px);
  border-color: var(--color-secondary);
  box-shadow:
    0 12px 35px rgba(0, 0, 0, 0.3),
    0 0 20px rgba(1, 242, 255, 0.15);
}

.btn-main {
  position: relative;
  overflow: hidden;
}

.btn-main::before {
  content: '';
  position: absolute;
  top: 0;
  left: -100%;
  width: 100%;
  height: 100%;
  background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.2), transparent);
  transition: left 0.5s ease;
}

.btn-main:hover::before {
  left: 100%;
}

.btn-outline {
  position: relative;
  overflow: hidden;
}

.btn-outline::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: linear-gradient(135deg, rgba(1, 242, 255, 0.05), transparent);
  opacity: 0;
  transition: opacity 0.3s ease;
}

.btn-outline:hover::before {
  opacity: 1;
}

.trust-item {
  position: relative;
  padding: 0.5rem 0;
}

.trust-item::after {
  content: '';
  position: absolute;
  bottom: 0;
  left: 0;
  width: 0;
  height: 2px;
  background: linear-gradient(90deg, var(--color-secondary), transparent);
  transition: width 0.3s ease;
}

.trust-item:hover::after {
  width: 100%;
}

.trust-num {
  transition: all 0.3s ease;
}

.trust-item:hover .trust-num {
  text-shadow: 0 0 20px rgba(1, 242, 255, 0.5);
}

@media (max-width: 1100px) {
  .hero-heading {
    animation: fadeInUp 0.8s ease-out;
  }

  .visual-card {
    animation: fadeInUp 0.8s ease-out 0.3s both;
  }
}

@media (max-width: 640px) {
  .hero-heading {
    font-size: 2.2rem;
  }

  .hero-text {
    font-size: 1rem;
  }

  .cta-wrapper {
    flex-direction: column;
    gap: 0.8rem;
  }

  .btn-main,
  .btn-outline {
    width: 100%;
    justify-content: center;
  }

  .trust-badges {
    flex-direction: column;
    gap: 1.2rem;
    align-items: center;
  }
}

@media (max-width: 480px) {
  .hero-container {
    padding: 4rem 1.5rem;
  }

  .badge {
    font-size: 0.7rem;
    padding: 0.5rem 1rem;
  }

  .hero-heading {
    font-size: 1.8rem;
  }

  .hero-text {
    font-size: 0.9rem;
    line-height: 1.6;
  }

  .btn-main,
  .btn-outline {
    padding: 0.8rem 1.4rem;
    font-size: 0.9rem;
  }

  .trust-num {
    font-size: 1.4rem;
  }
}
</style>
