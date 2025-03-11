<script setup>

const props = defineProps({

    name: String,
    date: String,
    link: String

});

const goToLink = () => {
    window.open(props.link, '_blank');
};

</script>

<template>

    <div class="group col-span-12 md:col-span-12 xl:col-span-6 bg-primary text-white rounded-t-2xl motion-preset-fade  motion-duration-1500 transition delay-150 duration-300 ease-in-out hover:-translate-y-1 hover:scale-105    ">
        
        <div class="relative">
            <slot></slot>

            <div @click="goToLink" class="group-hover:flex group-hover:transition-all delay-150 duration-300 ease-in-out hidden rounded-t-2xl transition-all justify-center items-center absolute top-0 w-full h-full  p-3 bg-[rgba(0,0,0,0.5)]">
                <i class="bi bi-play-circle text-5xl motion-preset-pop "></i>
            </div>
        </div>

        <div class="p-3 text-xl">
            <p class="pb-2">{{name}}</p>
            <p class="text-ternary font-semibold">{{date}}</p>
        </div>
    </div>

</template>

<style scoped></style>
