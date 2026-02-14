<script setup>
import { data } from "@/composables/projects";
import { ref } from "vue";
import index from '@/assets/Projects/index.png';
const emit = defineEmits(["toggle"]);

const toggle = () => {
  emit("toggle");
};

const total_projects = ref(data.length);

const preview = ref(data[total_projects.value - 1]);

const showPreview = ref(false);

const iconColor = ref('D652E9')
</script>

<template>
  <!-- Use explicit columns on large screens so the layout doesn't look stretched/wonky on wide displays -->
  <div class="grid gap-4 text-white motion-preset-fade grid-cols-1 lg:grid-cols-2 xl:grid-cols-4 auto-rows-fr">
    <div class="flex flex-col gap-4 xl:col-span-1">
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
          <p class="text-center text-5xl p-4">1</p>
        </div>
      </div>
    </div>

    <!-- About spanning 2 columns on xl keeps it readable on large screens -->
    <div class="bg-primary rounded-xl p-4 motion-preset-slide-right motion-duration-800 xl:col-span-2">
      <p class="font-bold pb-6 text-xl">About</p>
      <p class="text-overflow-ellipsis sm:text-lg">
        &emsp;&emsp;A programmer solely focused on backend development. My goal for every project is to learn something
        new, and the
        knowledge gained contributes to my continuous self-improvement.
      </p>
    </div>

    <!-- Latest project stays compact and image is constrained to avoid huge empty space on wide screens -->
    <div class="bg-primary rounded-xl p-4 motion-preset-slide-right motion-duration-600 xl:col-span-1">
      <p class="font-bold pb-6 text-xl">Latest Project</p>
      <div class="w-full flex justify-center overflow-hidden">
        <div class="relative group w-full">
          <img class="w-full rounded-lg object-cover max-h-52 sm:max-h-64 xl:max-h-56" :src="index" alt="" />
          <div
            class="group-hover:opacity-100 z-100 opacity-0 flex justify-center items-center absolute top-0 w-full h-full p-3 bg-[rgba(0,0,0,0.8)] scale-90 group-hover:scale-100 transition-all duration-400 ease-in-out">
            <button @click="toggle"
              class="p-3 px-6 rounded-2xl font-semibold bg-ternary backdrop-blur-xl border border-[rgba(255,255,255,0.3)] shadow-[0_4px_30px_rgba(0,0,0,0.1)] transition-all duration-300 ease-in-out hover:bg-ternary hover:scale-105">
              Preview
            </button>

          </div>

          <div class="absolute flex flex-col inset-0 items-center text-center h-full">
            <!-- centered overlay image (resized) -->
            <div class="w-full px-4 py-3 bg-gradient-to-b from-black/70 via-black/20 to-transparent ">
              <p class=" font-semibold font-secondary leading-tight text-xl text-ternary/70">
                {{ preview.display_name }}
              </p>
            </div>

            <div>

              <img v-if="preview.image_display !== 'portrait'" :src="preview.image"
                class="w-65 sm:w-55 md:w-80 lg:w-65 xl:w-55 object-contain opacity-90 rounded" alt="" />
              <img v-else :src="preview.image" class="w-25 object-contain opacity-90">
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="flex flex-col gap-4 xl:col-span-1">
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
        <div class="flex gap-4 w-full">
          <input type="text" placeholder="Send me a message..."
            class="grow bg-secondary text-white outline-none p-3 rounded-xl">
          <button class="bg-ternary p-3 rounded-xl hover:bg-ternary/60 cursor-pointer">Send</button>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped></style>
