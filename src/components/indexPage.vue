<template>
    <div class="h-dvh w-dvw bg-secondary font-primary overflow-x-hidden overflow-y-hidden ">

        <div class="flex h-full">
            <div class="bg-primary  w-fit sm:w-md flex justify-center p-4 rounded-br-3xl rounded-tr-3xl motion-preset-slide-right ">
                <div class="flex flex-col w-fit h-fit text-xl text-white pt-10 items-center sm:items-start">
                    <div class="flex flex-col pb-10 sm:pb-0 sm:items-center gap-9">
                        <div class="w-8 sm:w-28 ">
                            <img class="rounded-full w-full " src="../assets/media/profile.png" alt="">
                        </div>

                        <div class="pb-14 font-semibold hidden sm:block ">Rencell Tobelonia</div>
                    </div>

                    <ul class="flex flex-col gap-9">
                        <li @click="activeTab = 1" :class="[activeTab == 1 ? 'text-ternary drop-shadow-[0px_0px_3px_rgba(214,82,233,1)]' : 'text-white']"
                            class="hover:cursor-pointer">
                            <i class="bi bi-house-fill inline-block w-fit sm:w-8 "></i><p class="hidden sm:inline-block">Home</p></li>
                        <li @click="activeTab = 2" :class="[activeTab == 2 ? 'text-ternary drop-shadow-[0px_0px_3px_rgba(214,82,233,1)]' : 'text-white']"
                            class="hover:cursor-pointer"><i class="bi bi-info-circle-fill inline-block w-fit sm:w-8"></i><p class="hidden sm:inline-block">About</p>
                        </li>
                        <li @click="activeTab = 3" :class="[activeTab == 3 ? 'text-ternary drop-shadow-[0px_0px_3px_rgba(214,82,233,1)]' : 'text-white']"
                            class="hover:cursor-pointer"><i class="bi bi-code-slash inline-block w-fit sm:w-8"></i><p class="hidden sm:inline-block">Projects</p></li>
                        <li @click="activeTab = 4" :class="[activeTab == 4 ? 'text-ternary drop-shadow-[0px_0px_3px_rgba(214,82,233,1)]' : 'text-white']"
                            class="hover:cursor-pointer"><i class="bi bi-telephone-fill inline-block w-fit sm:w-8"></i><p class="hidden sm:inline-block">Contacts</p>
                        </li>
                    </ul>
                </div>

            </div>
            <div class="bg-secondary w-full p-6 sm:p-13 overflow-scroll 
            [&::-webkit-scrollbar]:w-2
            [&::-webkit-scrollbar-track]:rounded-full
            [&::-webkit-scrollbar-thumb]:rounded-full
            [&::-webkit-scrollbar-track]:bg-secondary
            [&::-webkit-scrollbar-thumb]:bg-ternary
            dark:[&::-webkit-scrollbar-track]:bg-secondary
            dark:[&::-webkit-scrollbar-thumb]:bg-ternary
            snap-y snap-mandatory">
                <component :is="showComponent" @toggle="goToProjectTab"></component>
            </div>
        </div>


    </div>
</template>

<script setup>
import homeTab from './main/homeTab.vue';
import aboutTab from './main/aboutTab.vue';
import projectTab from './main/projectTab.vue';
import contactTab from './main/contactTab.vue';
import { computed, ref } from 'vue';

const activeTab = ref(1);
const components = [homeTab, aboutTab, projectTab, contactTab]
const showComponent = computed(() => {

    return components[activeTab.value - 1]
});

const goToProjectTab = () => {

    activeTab.value = 3
}



</script>

<style scoped></style>
