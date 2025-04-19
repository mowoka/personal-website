<script setup>
import Counter from "./components/layout/Counter.vue";
import HeroSection from "./components/layout/HeroSection.vue";
import Navbar from "./components/layout/Navbar.vue";
import Service from "./components/layout/Service.vue";
</script>

<template>
  <div class="bg-[#d4ebf8] dark:bg-[#080326] min-h-screen">
    <Navbar />
    <HeroSection />
    <Counter />
    <Service />
  </div>
</template>
