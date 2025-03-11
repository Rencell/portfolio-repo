<script setup>
import { data } from "@/composables/projects";
import { ref } from "vue";

const emit = defineEmits(["toggle"]);

const toggle = () => {
  emit("toggle");
};

const total_projects = ref(data.length);

const generate_random_number = ref(
  parseInt(Math.random() * total_projects.value + 0)
);
const preview_image = ref(data[total_projects.value - 1].image);

const showPreview = ref(false);
</script>

<template>
  <div class="grid grid-cols-12 gap-4 text-white motion-preset-fade">
    <div class="col-span-12 sm:col-span-6 flex flex-col gap-4">
      <p class="text-4xl font-bold">Hello, Welcome.</p>
      <p class="text-2xl font-bold bg-ternary w-fit px-2 motion-preset-bounce">
        My Portfolio
      </p>
      <div class="flex gap-4 h-full pt-4">
        <div
          class="bg-primary p-2 rounded-xl text-sm sm:text-xl font-bold grow motion-preset-slide-right motion-duration-1000"
        >
          <p>Total Projects</p>
          <p class="text-center text-5xl p-4" v-text="total_projects"></p>
        </div>
        <div
          class="bg-primary p-2 rounded-xl text-sm sm:text-xl font-bold grow motion-preset-slide-right motion-duration-800"
        >
          <p>Ongoing Projects</p>
          <p class="text-center text-5xl p-4">0</p>
        </div>
      </div>
    </div>
    <div
      class="col-span-12 sm:col-span-6 bg-primary rounded-xl p-4 motion-preset-slide-right motion-duration-800"
    >
      <p class="font-bold pb-6 text-xl">About</p>
      <p class="text-overflow-ellipsis sm:text-lg">
        &emsp;&emsp;Hello, I'm a programmer solely focused on backend
        development and somewhat involved in web designing. My goal for every
        project is to learn something new, and the knowledge gained contributes
        to my continuous self-improvement.
      </p>
    </div>
    <div
      class="col-span-12 sm:col-span-6 bg-primary rounded-xl p-4 motion-preset-slide-right motion-duration-1000"
    >
      <p class="font-bold pb-6 text-xl">Latest Project</p>
      <div class="w-full flex justify-center">
        <div class="relative group">
          <img class="w-full" :src="preview_image" alt="" />
          <div
            class="group-hover:flex hidden delay-150 duration-300 ease-in-out group-hover:transition-all transition-all justify-center items-center absolute top-0 w-full h-full bga p-3 bg-[rgba(0,0,0,0.8)]"
          >
            <button
              @click="toggle"
              class="p-3 px-6 rounded-2xl font-semibold bg-ternary"
            >
              Preview
            </button>
          </div>
        </div>
      </div>
    </div>
    <div class="col-span-12 sm:col-span-6 flex flex-col gap-4">
      <div
        class="bg-primary rounded-xl grow p-4 motion-preset-slide-right motion-duration-600"
      >
        <p class="font-bold pb-6 text-xl">Current Techstack</p>

        <div class="grid grid-cols-6 sm:grid-cols-7 gap-2">
          <div class="p-3 rounded-full bg-secondary w-10 sm:w-fit">
            <img
              height="20"
              width="20"
              src="https://cdn.simpleicons.org/django/9b59b6"
            />
          </div>
          <div class="p-3 rounded-full bg-secondary w-10 sm:w-fit">
            <img
              height="20"
              width="20"
              src="https://cdn.simpleicons.org/vuedotjs/9b59b6"
            />
          </div>
          <div class="p-3 rounded-full bg-secondary w-10 sm:w-fit">
            <img
              height="20"
              width="20"
              src="https://cdn.simpleicons.org/htmx/9b59b6"
            />
          </div>
          <div class="p-3 rounded-full bg-secondary w-10 sm:w-fit">
            <img
              height="20"
              width="20"
              src="https://cdn.simpleicons.org/tailwindcss/9b59b6"
            />
          </div>
          <div class="p-3 rounded-full bg-secondary w-10 sm:w-fit">
            <img
              height="20"
              width="20"
              src="https://cdn.simpleicons.org/daisyui/9b59b6"
            />
          </div>
          <div class="p-3 rounded-full bg-secondary w-10 sm:w-fit">
            <img
              height="20"
              width="20"
              src="https://cdn.simpleicons.org/git/9b59b6"
            />
          </div>
          <div class="p-3 rounded-full bg-secondary w-10 sm:w-fit">
            <img
              height="20"
              width="20"
              src="https://cdn.simpleicons.org/postgresql/9b59b6"
            />
          </div>
          <div class="p-3 rounded-full bg-secondary w-10 sm:w-fit">
            <img
              height="20"
              width="20"
              src="https://cdn.simpleicons.org/fedora/9b59b6"
            />
          </div>
        </div>
      </div>
      <div
        class="bg-primary rounded-xl grow p-4 motion-preset-slide-right motion-duration-400"
      >
        <p class="font-bold pb-6 text-xl">Contact</p>
      </div>
    </div>
  </div>
</template>

<style scoped></style>
