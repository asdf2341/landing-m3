<template>
  <ScrollToTop />
  <Header />
  <HeroSection />
  <Principles />
  <Testimonials />
  <Projects />
  <FAQ />
  <Contact />
  <Footer />
</template>

<script>
import Header from '@/components/Header.vue'
import HeroSection from '@/components/HeroSection.vue'
// ... import others
export default {
  components: {
    Header,
    HeroSection,
    Principles,
    Testimonials,
    Projects,
    FAQ,
    Contact,
    Footer
}
</script>
