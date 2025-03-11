<script setup>
import { onMounted, ref } from 'vue';
const relativeElipsis = "after:content-[' s'] after:p-1.5 after:sm:p-2 after:absolute after:top-0 after:-left-8 after:bg-ternary after:rounded-full"

const showAnimation = ref(true)

onMounted(() =>{
    const snapelem = document.querySelectorAll(".snap-center");
    
    const observer = new IntersectionObserver((entries)=>{
        entries.forEach(entry => {
            if(entry.isIntersecting)
                showAnimation.value = entry.target.id == "1";
                
        })
    }, {
        threshold:0.5
    })
    
    snapelem.forEach(snap =>{
        observer.observe(snap)
    });

});


</script>

<template>

    <div id="1" class="text-white flex flex-col-reverse gap-4 pt-0 justify-center h-dvh snap-center relative items-center sm:items-start sm:flex-row sm:pt-32 "
        :class="[{'motion-preset-fade' :  showAnimation}] ">
        <div class="w-fit sm:w-xl pt-7 flex flex-col gap-8 ">
            <p class="text-lg sm:text-2xl font-bold">Hey, I'm <span class="italic text-ternary">Rencell</span></p>

            <div class="text-sm sm:text-lg">
                I'm Rencell Tobelonia, currently studying Information Technology at Cavite State University. Computers
                excite me every time I encounter something to troubleshoot or bugs to fix. I'm deeply passionate about
                my course, having been immersed in the world of computers since I was a kid.
            </div>

            <div class="w-full sm:w-sm">
                <div class="grid grid-cols-5 sm:grid-cols-6 gap-4 motion-preset-focus ">
                    <div class="p-3 rounded-full bg-primary w-10 sm:w-fit">
                        <img class="w-8" src="https://cdn.simpleicons.org/html5/9b59b6" />
                    </div>
                    <div class="p-3 rounded-full bg-primary w-10 sm:w-fit">
                        <img class="w-8" src="https://cdn.simpleicons.org/css/9b59b6" />
                    </div>
                    <div class="p-3 rounded-full bg-primary w-10 sm:w-fit">
                        <img class="w-8" src="https://cdn.simpleicons.org/javascript/9b59b6" />
                    </div>
                    <div class="p-3 rounded-full bg-primary w-10 sm:w-fit">
                        <img class="w-8" src="https://cdn.simpleicons.org/Python/9b59b6" />
                    </div>
                    <div class="p-3 rounded-full bg-primary w-10 sm:w-fit">
                        <img class="w-8" src="https://cdn.simpleicons.org/tailwindcss/9b59b6" />
                    </div>
                    <div class="p-3 rounded-full bg-primary w-10 sm:w-fit">
                        <img class="w-8" src="https://cdn.simpleicons.org/bootstrap/9b59b6" />
                    </div>
                    <div class="p-3 rounded-full bg-primary w-10 sm:w-fit">
                        <img class="w-8" src="https://cdn.simpleicons.org/php/9b59b6" />
                    </div>
                    <div class="p-3 rounded-full bg-primary w-10 sm:w-fit">
                        <img class="w-8" src="https://cdn.simpleicons.org/vuedotjs/9b59b6" />
                    </div>
                </div>
            </div>
        </div>

        <div class="w-32 sm:w-64"> <img class="w-full rounded-full" src="../../assets/media/profile.png" alt=""></div>

        <i class="bi bi-chevron-double-down absolute text-xl sm:text-4xl h-fit text-ternary bottom-5 motion-preset-oscillate "></i>
    </div>

    <div id="2" class="w-full h-dvh snap-center ">

        <div class="grid grid-cols-12 pt-15 w-full gap-0 sm:gap-10 gap-y-5">
            <div class="col-span-12 md:col-span-12 xl:col-span-6 ">
                <p class="text-4xl font-bold text-white pb-10 w-fit">Education</p>
                <div class="border-l-2 ps-6 border-primary flex flex-col gap-4 text-sm sm:text-lg">
                    <div class="text-white bg-primary rounded-3xl p-3  relative flex flex-col gap-1"
                        :class="[relativeElipsis, {'motion-preset-slide-right motion-duration-400' :  !showAnimation}] ">
                        <p class="font-bold text-ternary">Junior Highschool</p>
                        <p>2016-2020</p>
                        <p>• City of Bacoor National High School Springville</p>
                    </div>

                    <div class="text-white bg-primary rounded-3xl p-3  relative flex flex-col gap-1"
                        :class="[relativeElipsis, {'motion-preset-slide-right motion-duration-500' :  !showAnimation}]">
                        <p class="font-bold text-ternary">Senior Highschool</p>
                        <p>2020-2022</p>
                        <p>• Informatics College Imus Cavite</p>
                    </div>
                    <div class="text-white bg-primary rounded-3xl p-3  relative flex flex-col gap-1"
                        :class="[relativeElipsis, {'motion-preset-slide-right motion-duration-600' :  !showAnimation}]">
                        <p class="font-bold text-ternary">College</p>
                        <p>2022-2025</p>
                        <p>• Cavite State University - Bacoor Campus</p>
                    </div>

                </div>
            </div>
            <div class="col-span-12 md:col-span-12 xl:col-span-6">
                <p class="text-4xl font-bold text-white pb-10">Work</p>
                <div class="border-l-2 ps-6 border-primary flex flex-col gap-4">
                    <div class="text-white bg-primary rounded-3xl p-3  relative flex flex-col gap-1"
                        :class="[relativeElipsis, {'motion-preset-slide-right motion-duration-700' :  !showAnimation}] ">
                        Empty
                    </div>
                </div>

            </div>
        </div>


    </div>
</template>

<style scoped>



</style>
