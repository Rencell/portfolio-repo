<template>
    <div class="h-dvh w-dvw bg-secondary font-primary overflow-x-hidden overflow-y-hidden ">

        <div class="flex h-full">
            <div
                class="bg-primary w-md flex justify-center p-5 rounded-br-3xl rounded-tr-3xl motion-preset-slide-right ">
                <div class="flex flex-col w-fit h-fit text-xl text-white pt-10">
                    <div class="flex flex-col items-center gap-9">
                        <div class="w-28 ">
                            <img class="rounded-full w-full " src="../assets/media/profile.png" alt="">
                        </div>

                        <div class="pb-14 font-semibold">Rencell Tobelonia</div>
                    </div>

                    <ul class="flex flex-col gap-9">
                        <li @click="activeTab = 1" :class="[activeTab == 1 ? 'text-ternary' : text - white]"
                            class="hover:cursor-pointer" style="text-shadow: rgba(156,89,182,0.42) 0px 0px 7px;"><i
                                class="bi bi-house-fill inline-block w-8"></i>Home</li>
                        <li @click="activeTab = 2" :class="[activeTab == 2 ? 'text-ternary' : text - white]"
                            class="hover:cursor-pointer"><i class="bi bi-info-circle-fill inline-block w-8"></i>About
                        </li>
                        <li @click="activeTab = 3" :class="[activeTab == 3 ? 'text-ternary' : text - white]"
                            class="hover:cursor-pointer"><i class="bi bi-code-slash inline-block w-8"></i>Projects</li>
                        <li @click="activeTab = 4" :class="[activeTab == 4 ? 'text-ternary' : text - white]"
                            class="hover:cursor-pointer"><i class="bi bi-telephone-fill inline-block w-8"></i>Contacts
                        </li>
                    </ul>
                </div>

            </div>
            <div class="bg-secondary w-full p-13 overflow-scroll overflow-x-hidden
            [&::-webkit-scrollbar]:w-2
            [&::-webkit-scrollbar-track]:rounded-full
            [&::-webkit-scrollbar-track]:bg-gray-100
            [&::-webkit-scrollbar-thumb]:rounded-full
            [&::-webkit-scrollbar-thumb]:bg-gray-300
            dark:[&::-webkit-scrollbar-track]:bg-secondary
            dark:[&::-webkit-scrollbar-thumb]:bg-ternary
            snap-y snap-mandatory">
                <component :is="showComponent"></component>
            </div>
        </div>


    </div>
</template>

<script setup>
import homeTab from './main/homeTab.vue';
import aboutTab from './main/aboutTab.vue';
import projectTab from './main/projectTab.vue';
import { computed, ref } from 'vue';

const activeTab = ref(1);
const components = [homeTab, aboutTab, projectTab]
const showComponent = computed(() => {

    return components[activeTab.value - 1]
});



</script>

<style scoped></style>
