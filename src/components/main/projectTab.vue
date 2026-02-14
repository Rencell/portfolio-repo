<script setup>
import proj_component from '../../components/main/projectComponent/component.vue'
import { data } from '@/composables/projects';
import shibss from '@/assets/Projects/shibals.png';
import shibs from '@/assets/Projects/shibs.png';
import index from '@/assets/Projects/index.png';
</script>

<template>

    <div>
        <p class="text-2xl font-bold text-white pb-5">My Projects</p>
        <div class="grid grid-auto-fit-xl gap-5">
            <proj_component v-for="project in data" 
                :key="project.id" 
                :name="project.name" 
                :date="project.date"
                :link="project.link">

                <!-- image as background -->
                <div class="relative w-full h-full">
                    <img class="w-full h-full object-cover" :src="index" :alt="project.name" />

                    <div class="absolute flex flex-col inset-0 items-center text-center h-full">
                         <!-- centered overlay image (resized) -->
                        <div class="w-full px-4 py-3 bg-gradient-to-b from-black/70 via-black/20 to-transparent ">
                            <p class=" font-semibold font-secondary leading-tight text-xl text-ternary/70">
                                {{ project.display_name }}
                            </p>
                        </div>

                        <div>
                            
                            <img
                            v-if="project.image_display !== 'portrait'"
                            :src="project.image"
                            class="w-65 sm:w-55 md:w-80 lg:w-65 xl:w-55 object-contain opacity-90 rounded"
                            alt=""
                            />
                            <img v-else :src="project.image" class="w-25 object-contain opacity-90">
                        </div>
                    </div>
                </div>

            </proj_component>
        </div>
    </div>

</template>

<style scoped></style>
