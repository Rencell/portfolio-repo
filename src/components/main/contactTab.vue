w-fit sm:w-8<script setup>
</script>

<template>

    <div class="grid grid-cols-12 gap-4 text-white h-full items-center">
        <div class="col-span-12 md:col-span-6 xl:col-span-6">
            <p class="text-7xl font-bold pb-10 motion-preset-slide-down sm:motion-preset-slide-right">Contact Me</p>

            <p class="text-lg pb-3  motion-preset-slide-down sm:motion-preset-slide-right "><i class="bi bi-envelope-fill text-ternary text-xl"></i> Rencelltobelonia67@gmail.com</p>
            <p class=" motion-preset-slide-down sm:motion-preset-slide-right "><i class="bi bi-telephone-fill text-ternary text-xl"></i> 0994-719-6625</p>
            <div class="text-3xl flex gap-5 text-ternary pt-10 motion-preset-slide-down sm:motion-preset-slide-right">
                <i class="bi bi-facebook "></i>
                <i class="bi bi-github "></i>
                <i class="bi bi-messenger "></i>
                <i class="bi bi-youtube "></i>
                
            </div>
    
        </div>
    
        <div class=" grow col-span-12 md:col-span-6 xl:col-span-6 flex flex-col gap-4 motion-preset-slide-down pb-5 sm:pb-0" >
            <input type="text" class="p-4 bg-primary rounded-xl text-xs outline-0 " placeholder="Anonymous Name">
            <input type="text" class="p-4 bg-primary rounded-xl text-xs outline-0 " placeholder="Subject">
            <textarea name="" id="" class="p-4 bg-primary rounded-xl text-xs outline-0" placeholder="Message"></textarea>
            <button class="bg-ternary p-3 w-fit rounded-full text-sm px-7 motion-preset-slide-down  motion-duration-1400"> Submit </button>
        </div>
    </div>
</template>

<style scoped>
</style>