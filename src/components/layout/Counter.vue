<template>
  <section class="mt-20 lg:mt-0 relative text-white flex justify-center">
    <header
      class="absolute w-1/2 aspect-[16/5] -skew-x-12 rounded-full bg-gradient-to-r from-[#00c6cc] via-[#785ae4] to-secondary opacity-30 blur-[100px] left-10 top-0 hidden md:block"
    ></header>
    <header
      class="absolute w-1/2 aspect-[16/5] -skew-x-12 rounded-full bg-gradient-to-r from-[#00c6cc] via-[#785ae4] to-secondary opacity-30  blur-[100px] right-10 bottom-0 hidden md:block"
    ></header>

    <ul
      ref="statsSection"
      class="relative z-1 p-6 mx-auto w-11/12 lg:mx-0 rounded-3xl border bg-[#ffffff29] shadow-lg md:divide-x grid grid-cols-2 md:grid-cols-4 gap-4 md:gap-8 lg:gap-12 border-secondary divide-secondary"
    >
      <li class="text-center" v-for="element in numbers" :key="element.id">
        <h2
          class="font-semibold flex justify-center text-xl sm:text-2xl md:text-4xl w-full"
        >
          + <Countup v-if="hasInterested" :endVal="element.numbers" />
        </h2>
        <p class="mt-2">{{ element.title }}</p>
      </li>
    </ul>
  </section>
</template>

<script setup>
import { ref, onMounted } from "vue";

const numbers = ref([
  { id: 1, numbers: 2, title: "Company" },
  { id: 1, numbers: 8, title: "Projects Based" },
  { id: 1, numbers: 3, title: "Dedicated Projects" },
  { id: 1, numbers: 4, title: "Years Experience" },
]);

const statsSection = ref(null);
const hasInterested = ref(false);

onMounted(() => {
  const observer = new IntersectionObserver(
    ([entries]) => {
      if (entries.isIntersecting) {
        hasInterested.value = true;
        observer.disconnect();
      }
    },
    { threshold: 0.5 }
  );

  if (statsSection.value) {
    observer.observe(statsSection.value);
  }
});
</script>
