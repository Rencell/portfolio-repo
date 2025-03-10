<script setup>

const props = defineProps({

    name: String,
    date: String,

});

</script>

<template>

    <div class="col-span-12 md:col-span-12 xl:col-span-6 bg-primary text-white rounded-t-2xl motion-preset-fade   motion-duration-1500">
        
        <div>
            <slot></slot>
        </div>

        <div class="p-3 text-xl">
            <p class="pb-2">{{name}}</p>
            <p class="text-ternary font-semibold">{{date}}</p>
        </div>
    </div>

</template>

<style scoped></style>
