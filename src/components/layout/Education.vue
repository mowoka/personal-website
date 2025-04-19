<template>
  <section class="p-4 md:p-16">
    <header class="text-center">
      <h2 class="text-4xl font-bold text-white">Education</h2>
    </header>
    <ul class="mt-10 space-y-8">
      <li
        class="w-full rounded-xl shadow-lg border bg-gradient-to-t to-[#acac39] from-[#1f1e1c99]"
        v-for="(education, index) in educations"
        :key="index"
      >
        <article
          class="flex flex-col lg:flex-row items-center lg:items-start rounded-[12px] bg-primary mt-[3px] mx-[3px] p-6 md:p-8 lg:p-10"
        >
          <figure
            class="w-full lg:w-1/4 flex justify-center lg:justify-start mb-4 lg:mb-0"
          >
            <Icon
              icon="hugeicons:university"
              class="text-4xl md:text-6xl lg:text-7xl text-secondary"
            />
          </figure>

          <section class="w-full lg:w-3/4 lg:pl-4 text-center lg:text-left">
            <header>
              <h3
                class="text-xl md:text-2xl font-semibold uppercase text-secondary"
              >
                {{ education.school }}
              </h3>
            </header>
            <p class="text-sm md:text-base text-white">
              {{ education.degree }}
            </p>
            <p class="text-sm md:text-base text-white">
              {{ education.duration }}
            </p>
          </section>
        </article>
      </li>
    </ul>
  </section>
</template>

<script setup>
import { ref } from "vue";

const educations = ref([
  {
    duration: "January 2021 - Maret 2021",
    school: "Bootcamp Dumbways",
    degree: "Fullstack Developer",
  },
  {
    duration: "2012 - 2015",
    school: "SMK TI Pembangunan Cimahi",
    degree: "computer and network engineering",
  },
]);
</script>
