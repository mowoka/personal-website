<template>
  <section class="mt-32" id="skills">
    <SectionHeader title="My Skills" />
    <div class="mt-20 flex justify-center">
      <ul class="flex flex-wrap justify-center items-center">
        <li
          v-for="(skill, index) in skills"
          :key="index"
          :class="`mx-[15px] rounded-[12px] mb-7 bg-gradient-to-t ${skill.bgGradient}`"
        >
          <div
            class="rounded-[12px] bg-primary mt-[3px] p-12 md:p-5 text-center"
          >
            <h3
              class="font-bold text-[35px] text-white flex items-center justify-centers"
              :style="{ color: skill.textColor }"
            >
              {{ skill.title }}
            </h3>
          </div>
        </li>
      </ul>
    </div>
  </section>
</template>
<script setup>
import { onMounted, ref } from "vue";
import SectionHeader from "../UI/SectionHeader.vue";

const skills = ref([
  {
    title: "Figma",
    bgGradient: "to-[#acac39] from-[#1f1e1c99]",
    textColor: "#FFE600",
  },
  {
    title: "Java",
    bgGradient: "to-[#00a9ff99] from-[#1f1e1c99]",
    textColor: "#59c378",
  },
  {
    title: "Photoshop",
    bgGradient: "to-[#dd584f99] from-[#1f1e1c99]",
    textColor: "#dd584f",
  },
  {
    title: "Vue js",
    bgGradient: "to-[#ff9a0099] from-[#1f1e1c99]",
    textColor: "#ff9a00",
  },
  {
    title: "Wordpress",
    bgGradient: "to-[#00a9ff99] from-[#1f1e1c99]",
    textColor: "#00a9ff",
  },
  {
    title: "ReactJS",
    bgGradient: "to-[#9e00ff99] from-[#1f1e1c99]",
    textColor: "#ad00ff",
  },
  {
    title: "HTML",
    bgGradient: "to-[#acac39] from-[#1f1e1c99]",
    textColor: "#ffe600",
  },
  {
    title: "Javascript",
    bgGradient: "to-[#59c37899] from-[#1f1e1c99]",
    textColor: "#59c378",
  },
]);

</script>
<style></style>
