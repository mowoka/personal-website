<template>
  <section class="mt-32" id="contact">
    <SectionHeader title="Contact Me" />
    <div class="py-8 lg:py-16 px-4 mx-auto max-w-screen-md">
      <form class="space-y-8">
        <div v-for="(input, index) in inputs" :key="index">
          <Input
            :id="input.id"
            :label="input.label"
            :type="input.type"
            :placeholder="input.placeholder"
            :rows="input.rows"
          />
        </div>
        <div class="flex justify-between">
            <Button label="send" />

            <div class="mt-2 flex justify-center space-x-3 md:space-x-8">
                <a href="" class="text-gray-600 hover:text-blue-500" >
                    <Icon icon="fa-brands:twitter" style="font-size: 2rem;" />
                </a>
                <a href="" class="text-gray-600 hover:text-blue-700" >
                    <Icon icon="fa-brands:linkedin" style="font-size: 2rem;" />
                </a>
                <a href="" class="text-gray-600 hover:text-gray-800" >
                    <Icon icon="fa-brands:github" style="font-size: 2rem;" />
                </a>
                <a href="" class="text-gray-600 hover:text-pink-500" >
                    <Icon icon="fa-brands:instagram" style="font-size: 2rem;" />
                </a>
            </div>
        </div>
      </form>
    </div>
  </section>
</template>

<script setup>
import { ref } from "vue";
import SectionHeader from "../UI/SectionHeader.vue";
import Input from "../UI/Input.vue";
import Button from "../UI/Button.vue";

const inputs = ref([
  {
    id: "email",
    label: "your email",
    type: "email",
    placeholder: "example@gmail.com",
    rows: undefined,
  },
  {
    id: "Subject",
    label: "Subject",
    type: "text",
    placeholder: "Let us know how I can help you?",
    rows: undefined,
  },
  {
    id: "message",
    label: "Message",
    type: "textarea",
    placeholder: "Leave us comment",
    rows: 6,
  },
]);
</script>
