<script setup>
import { data } from "@/composables/projects";
import { ref } from "vue";

const emit = defineEmits(["toggle"]);

const toggle = () => {
  emit("toggle");
};

const total_projects = ref(data.length);

const preview_image = ref(data[total_projects.value - 1].image);

const showPreview = ref(false);

const iconColor = ref('D652E9')
</script>

<template>
  <div class="grid grid-auto-fit-xl gap-4 text-white motion-preset-fade">
    <div class="flex flex-col gap-4">
      <p class="text-4xl font-bold">Hello, Welcome.</p>
      <p class="text-2xl font-bold bg-ternary w-fit px-2 motion-preset-bounce">
        My Portfolio
      </p>
      <div class="flex gap-4 h-full pt-4">
        <div
          class="bg-primary p-2 rounded-xl text-sm sm:text-xl font-bold grow motion-preset-slide-right motion-duration-1000">
          <p>Total Projects</p>
          <p class="text-center text-5xl p-4" v-text="total_projects"></p>
        </div>
        <div
          class="bg-primary p-2 rounded-xl text-sm sm:text-xl font-bold grow motion-preset-slide-right motion-duration-800">
          <p>Ongoing Projects</p>
          <p class="text-center text-5xl p-4">0</p>
        </div>
      </div>
    </div>
    <div class="bg-primary rounded-xl p-4 motion-preset-slide-right motion-duration-800">
      <p class="font-bold pb-6 text-xl">About</p>
      <p class="text-overflow-ellipsis sm:text-lg">
        &emsp;&emsp;Hello, I'm a programmer solely focused on backend
        development and somewhat involved in web designing. My goal for every
        project is to learn something new, and the knowledge gained contributes
        to my continuous self-improvement.
      </p>
    </div>
    <div class="bg-primary rounded-xl p-4 motion-preset-slide-right motion-duration-1000">
      <p class="font-bold pb-6 text-xl">Latest Project</p>
      <div class="w-full flex justify-center">
        <div class="relative group">
          <img class="w-full" :src="preview_image" alt="" />
          <div class="group-hover:opacity-100 opacity-0 flex justify-center items-center absolute top-0 w-full h-full p-3 bg-[rgba(0,0,0,0.8)]
                      scale-90 group-hover:scale-100 transition-all duration-400 ease-in-out">
            <button @click="toggle" class="p-3 px-6 rounded-2xl font-semibold 
                bg-ternary backdrop-blur-xl 
                  border border-[rgba(255,255,255,0.3)] shadow-[0_4px_30px_rgba(0,0,0,0.1)] 
                  transition-all duration-300 ease-in-out 
                hover:bg-ternary hover:scale-105">
              Preview
            </button>

          </div>
        </div>
      </div>
    </div>
    <div class="flex flex-col gap-4">
      <div class="bg-primary rounded-xl grow p-4 motion-preset-slide-right motion-duration-600">
        <p class="font-bold pb-6 text-xl">Current Techstack</p>

        <div class="grid grid-cols-4 sm:grid-cols-6 gap-2">
          <div class="p-3 rounded-full bg-secondary w-10 sm:w-fit">
            <img height="20" width="20" :src="'https://cdn.simpleicons.org/django/' + iconColor" />
          </div>
          <div class="p-3 rounded-full bg-secondary w-10 sm:w-fit">
            <img height="20" width="20" :src="'https://cdn.simpleicons.org/vuedotjs/' + iconColor" />
          </div>
          <div class="p-3 rounded-full bg-secondary w-10 sm:w-fit">
            <img height="20" width="20" :src="'https://cdn.simpleicons.org/htmx/' + iconColor" />
          </div>
          <div class="p-3 rounded-full bg-secondary w-10 sm:w-fit">
            <img height="20" width="20" :src="'https://cdn.simpleicons.org/tailwindcss/' + iconColor" />
          </div>
          <div class="p-3 rounded-full bg-secondary w-10 sm:w-fit">
            <img height="20" width="20" :src="'https://cdn.simpleicons.org/daisyui/' + iconColor" />
          </div>
          <div class="p-3 rounded-full bg-secondary w-10 sm:w-fit">
            <img height="20" width="20" :src="'https://cdn.simpleicons.org/git/' + iconColor" />
          </div>
          <div class="p-3 rounded-full bg-secondary w-10 sm:w-fit">
            <img height="20" width="20" :src="'https://cdn.simpleicons.org/postgresql/' + iconColor" />
          </div>
          <div class="p-3 rounded-full bg-secondary w-10 sm:w-fit">
            <img height="20" width="20" :src="'https://cdn.simpleicons.org/fedora/' + iconColor" />
          </div>
        </div>
      </div>
      <div class="bg-primary rounded-xl grow p-4 motion-preset-slide-right motion-duration-400">
        <p class="font-bold pb-6 text-xl">Contact</p>
      </div>
    </div>
  </div>
</template>

<style scoped></style>
