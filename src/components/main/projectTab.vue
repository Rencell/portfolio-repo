<script setup>
import proj_component from '../../components/main/projectComponent/component.vue'
import { data } from '@/composables/projects';
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
                <img class="rounded-t-2xl" :src="project.image" :alt="project.name" />
            </proj_component>
        </div>
    </div>

</template>

<style scoped></style>
