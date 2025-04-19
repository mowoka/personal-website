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
          <div class="p-[30px]">
            <h3 class="uppercase font-semibold text-secondary text-base">{{ element.name }} </h3>
            <p class="text-[14px] leading-[20px] text-white tracking-[0.03rem]">{{ element.description }}</p>
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
      "lorem ipsum dolor sit amet consectetur adipisicing elit. Quas ad obcaecati dolor itaque unde adipisci alias ipsum voluptas debitis nostrum fugiat amet provident, est sapiente esse distinctio impedit! Provident, sit?",
  },
  {
    id: 2,
    icon: "dashicons:welcome-write-blog",
    name: "Technilca Writing",
    description:
      "lorem ipsum dolor sit amet consectetur adipisicing elit. Quas ad obcaecati dolor itaque unde adipisci alias ipsum voluptas debitis nostrum fugiat amet provident, est sapiente esse distinctio impedit! Provident, sit?",
  },
  {
    id: 3,
    icon: "logos:chrome-web-store",
    name: "Technilca Writing",
    description:
      "lorem ipsum dolor sit amet consectetur adipisicing elit. Quas ad obcaecati dolor itaque unde adipisci alias ipsum voluptas debitis nostrum fugiat amet provident, est sapiente esse distinctio impedit! Provident, sit?",
  },
  {
    id: 4,
    icon: "logos:chrome-web-store",
    name: "Technilca Writing",
    description:
      "lorem ipsum dolor sit amet consectetur adipisicing elit. Quas ad obcaecati dolor itaque unde adipisci alias ipsum voluptas debitis nostrum fugiat amet provident, est sapiente esse distinctio impedit! Provident, sit?",
  },
  {
    id: 5,
    icon: "logos:chrome-web-store",
    name: "Technilca Writing",
    description:
      "lorem ipsum dolor sit amet consectetur adipisicing elit. Quas ad obcaecati dolor itaque unde adipisci alias ipsum voluptas debitis nostrum fugiat amet provident, est sapiente esse distinctio impedit! Provident, sit?",
  },
]);
</script>
<style></style>
