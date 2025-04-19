<script setup>
import Contact from "./components/layout/Contact.vue";
import Counter from "./components/layout/Counter.vue";
import Footer from "./components/layout/Footer.vue";
import HeroSection from "./components/layout/HeroSection.vue";
import Navbar from "./components/layout/Navbar.vue";
import Projects from "./components/layout/Projects.vue";
import Service from "./components/layout/Service.vue";
import Skills from "./components/layout/Skills.vue";
import WhyMe from "./components/layout/WhyMe.vue";
</script>

<template>
  <div class="bg-[#d4ebf8] dark:bg-[#080326] min-h-screen">
    <Navbar />
    <HeroSection />
    <Counter />
    <Service />
    <Skills />
    <WhyMe />
    <Projects />
    <Contact />
    <Footer />
  </div>
</template>
