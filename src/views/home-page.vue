<script setup>
import HeroSection from '../components/hero_section.vue'
import AboutSection from '../components/about_section.vue'
import ServiceSection from '../components/service_section.vue'
import WorkSection from '../components/work_section.vue'
import ContactSection from '../components/contact_section.vue'
import FooterSection from '../components/footer_section.vue'
</script>
<template>
  <HeroSection />
  <AboutSection />
  <ServiceSection />
  <WorkSection />
  <ContactSection />
  <FooterSection />
</template>
<style>
:root {
  --color-primary: #01f2ff;
  --color-secondary: #54f0ff;
  --color-background: #020917;
  --color-text: #f8f9fb;
  --color-muted: #71879c;
}
body {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  background-color: #090b0d;
}
</style>
