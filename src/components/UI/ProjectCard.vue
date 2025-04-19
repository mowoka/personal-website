<template>
  <article
    class="max-w-sm overflow-hidden shadow-lg rounded border border-secondary dark:bg-[#ffffff29] bg-primary"
  >
    <!-- image section -->
    <figure>
      <!-- <img src="../../assets/images/monorepo-preview.png" :alt="title" class="w-full h-48 object-cover" /> -->
      <img :src="image" :alt="title" class="w-full h-48 object-cover" />
    </figure>

    <!-- content section -->
    <section class="px-6 py-4">
      <header>
        <h3 class="font-bold text-xl  text-white">{{ title }}</h3>
      </header>
      <p class="text-gray-300 text-sm">{{ description }}</p>
    </section>

    <!-- section tags -->

    <footer class="px-6 pt-4 pb-2">
      <ul class="flex flex-wrap gap-2">
        <li
          v-for="(tag, index) in tags"
          :key="index"
          class="inline-block dark:bg-primary bg-gray-700 rounded-full px-3 py-1 text-sm font-semibold text-white"
        >
          #{{ tag }}
        </li>
      </ul>
    </footer>

    <!-- actions section -->

    <div class="px-6 pb-4 flex justify-between items-center">
      <a
        :href="liveLink"
        v-if="liveLink"
        class="text-secondary font-semibold hover:underline text-sm"
        >Live Demo</a
      >
      <a
        :href="codeLink"
        v-if="codeLink"
        class="text-secondary font-semibold hover:underline text-sm"
        >View Code</a
      >
    </div>
  </article>
</template>

<script setup>
defineProps({
  title: {
    type: String,
    default: "Project Title",
    required: true,
  },
  description: {
    type: String,
    default: "Brief description",
    required: true,
  },
  image: {
    type: String,
    default: "/",
    required: true,
  },
  tags: {
    type: Array,
    required: false,
    default: ["vue js", "Tailwind Css"],
  },
  liveLink: {
    type: String,
    required: false,
    dafault: null,
  },
  codeLink: {
    type: String,
    required: false,
    dafault: null,
  },
});
</script>
