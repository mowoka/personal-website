<template>
  <section id="projects" class="relative w-11/12 px-16 mx-auto">
    <SectionHeader title="My Projects" />
    <!-- custom navigation buttons -->
    <button
      class="swiper-prev absolute top-2/3 left-4 transform -translate-y-1/2 z-10 text-white bg-secondary  p-4 rounded-full"
    >
      <Icon icon="line-md:arrow-left" class="font-bold text-2xl" />
    </button>
    <button
      class="swiper-next absolute top-2/3 right-4 transform -translate-y-1/2 z-10 text-white bg-secondary p-4 rounded-full"
    >
      <Icon icon="line-md:arrow-right" class="font-bold text-2xl" />
    </button>

    <!-- Swiper content -->
    <swiper
      :effect="'coverflow'"
      grabCursor
      centeredSlides
      :slidesPerView="'auto'"
      :coverflowEffect="{
        rotate: 50,
        stretch: 0,
        depth: 100,
        modifier: 1,
        slideShadows: true,
      }"
      :navigation="navigationOptions"
      loop
      pagination
      :modules="[EffectCoverflow, Navigation]"
      class="max-w-full mt-32"
    >
      <swiper-slide
        class="max-w-[300px]"
        v-for="(project, index) in projects"
        :key="index"
      >
        <ProjectCard
          :title="project.title"
          :description="project.description"
          :image="project.image"
          :tags="project.tags"
          :liveLink="project.liveLink"
          :codeLink="project.codeLink"
        />
      </swiper-slide>
    </swiper>
  </section>
</template>

<script setup>
import SectionHeader from "../UI/SectionHeader.vue";
import {ref} from 'vue';
import { EffectCoverflow, Navigation } from "swiper/modules";
import { Swiper, SwiperSlide } from "swiper/vue";
import "swiper/css";
import "swiper/css/effect-coverflow";
import "swiper/css/navigation";
import "swiper/css/pagination";
import ProjectCard from "../UI/ProjectCard.vue";
import WowPreview from '../../assets/images/wow-preview.png';
import WaysBookPreview from '../../assets/images/ways-book-preview.png';
import HelloRecipePreview from '../../assets/images/hello-recipe-app.png';
import MonorepoPreview from '../../assets/images/monorepo-osm.png';
import PersonalPreview from '../../assets/images/personal-website-preview.png';

// * Define Navigation
const navigationOptions = {
  prevEl: ".swiper-prev",
  nextEl: ".swiper-next",
};

const projects = ref([
  {
    title: "World of Books",
    description: "Window Of World is Web Library Online. Web applications that handle users who want to read. by paying only once and can read all books",
    image: WowPreview,
    tags: ["React JS", "Bootstrap Css", "Express JS", "Mysql"],
    liveLink: "/",
    codeLink: "https://github.com/mowoka/DWF20VBFK_WOW-PROJECT",
  },
  {
    title: "Ways Books",
    description: "WaysBook is web app point of sales book.  an application made to handle both the user and the admin page",
    image: WaysBookPreview,
    tags: ["React JS", "Bootstrap Css", "Express JS", "Mysql"],
    liveLink: "/",
    codeLink: "https://github.com/mowoka/batch20-FinalTask",
  },
  {
    title: "Hello Recipe App",
    description: "Mobile Apps helps customers to saving and reference food recipes",
    image: HelloRecipePreview,
    tags: ["Android", "IOS", "Flutter", "Unit Testing"],
    liveLink: "/",
    codeLink: "https://github.com/mowoka/flutter_movies",
  },
  {
    title: "Monorepo OSM Map",
    description: "Monorepo OpenStreetMap using Next JS, React Native Expo",
    image: MonorepoPreview,
    tags: ["Solito JS", "Next JS", "React Native", "Expo"],
    liveLink: "/",
    codeLink: "https://github.com/mowoka/monorepo_osm",
  },
  {
    title: "Personal Website",
    description: "Personal website for display profile giofanny mowoka",
    image: PersonalPreview,
    tags: ["Javascript", "Vue 3"],
    liveLink: "/",
    codeLink: "https://github.com/mowoka/personal-website",
  },
]);
</script>

<style scoped>
.swiper-button-prev,
.swiper-button-next{
    cursor: pointer;
}

.swiper-slide{
    display: flex;
    justify-content: center;
    align-items: center;
}
</style>
