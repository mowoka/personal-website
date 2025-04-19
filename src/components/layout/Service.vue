<template>
  <section id="services" class="relative text-white mt-32">
    <SectionHeader title="My Services" />
    <div
      class="mt-20 py-8 xl:px-16 px-4 sm:py-16 grid grid-cols-1 gap-6 pt-10 sm:grid-cols-2 md:gap-10 md:pt-12 lg:grid-cols-3"
    >
      <article
        class="px-[12px] mb-[24px]"
        v-for="element in services"
        :key="element.id"
      >
        <div
          data-aos="fade-up"
          :data-aos-delay="element.id * 100"
          class="mt-[30px] relative flex flex-col justify-center text-center rounded-[30px] border border-secondary dark:bg-[#ffffff29] bg-primay"
        >
          <div class="mt-[30px] flex justify-center relative">
            <div class="mt-[-7px] p-[8px] relative bg-primary rounded-[50%]">
              <span
                class="h-[60px] w-[60px] m-auto border-[1px] border-solid border-secondary rounded-[50%] flex justify-center items-center"
              >
              <Icon :icon="element.icon" class="text-[30px] relative z-[1]" />
            </span>
            </div>
          </div>
          <div class="px-[30px] pt-[10px] pb-[30px]">
            <h3 class="uppercase font-semibold text-secondary text-base">{{ element.name }} </h3>
            <p class="text-[14px] leading-[20px] text-white tracking-[0.03rem] mt-2">{{ element.description }}</p>
          </div>
        </div>
      </article>
    </div>
  </section>
</template>
<script setup>
import SectionHeader from "../UI/SectionHeader.vue";
import { ref } from "vue";

const services = ref([
  {
    id: 1,
    icon: "logos:chrome-web-store",
    name: "Web Development",
    description:
      "Develop web applications using (HTML, CSS, and Javascript), (React JS), (Next JS), (Vue JS) combine with TypeScript. Create responsive and visually appealing websites that are easy to navigate and use.",
  },
  {
    id: 2,
    icon: "fluent-emoji:mobile-phone",
    name: "Mobile Development",
    description:
      "Develop mobile applications using (React Native), (React Native Expo), (Flutter). Create application native support both device platform android and ios, pulish on apple store and google play store.",
  },
  {
    id: 3, 
    icon: "fa-solid:hands-helping",
    name: "Fullstack Development",
    description:
      "Develop fullstack applications using (Next JS), (React JS + Nest JS). Create responsive and visually appealing websites that are easy to navigate and use, and manage saving data to database.",
  },
  {
    id: 4,
    icon: "fxemoji:pages",
    name: "Slicing Pages",
    description:
      "Create slicing per page using (Grunt), (HTML, CSS, and Javascript). Create component library for reusable code and manage styling and design. create page layout per feature.",
  },
  {
    id: 5,
    icon: "logos:chrome-web-store",
    name: "IT Support",
    description:
      "Provide IT support for the website and application. Provide technical support for the website and application. Provide technical support for the website and application.",
  },
]);
</script>
<style></style>
