<script setup>
import BackToTop from "./components/layout/BackToTop.vue";
import Contact from "./components/layout/Contact.vue";
import Counter from "./components/layout/Counter.vue";
import Footer from "./components/layout/Footer.vue";
import HeroSection from "./components/layout/HeroSection.vue";
import Navbar from "./components/layout/Navbar.vue";
import Projects from "./components/layout/Projects.vue";
import Service from "./components/layout/Service.vue";
import Skills from "./components/layout/Skills.vue";
import WhyMe from "./components/layout/WhyMe.vue";
import LoadingSpinner from "./components/layout/LoadingSpinner.vue";
</script>

<template>
  <div class="bg-[#080326] min-h-screen">
    <Suspense>
      <template #default>
        <div>
          <Navbar />
          <HeroSection />
          <Counter />
          <Service />
          <Skills />
          <WhyMe />
          <Projects />
          <Contact />
          <Footer />
          <BackToTop />
        </div>
      </template>

      <template #fallback>
        <div class="flex justify-center items-center min-h-screen">
          <LoadingSpinner />
        </div>
      </template>
    </Suspense>
  </div>
</template>

<style>
*{
  scrollbar-width: thin;
  scrollbar-color: #111827 #f1f1f1;
}

</style>
