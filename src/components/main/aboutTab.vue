<script setup>
import { onMounted, ref } from 'vue';
const relativeElipsis = "after:content-[' s'] after:p-1.5 after:sm:p-1 after:md:p-1.5 after:absolute after:top-0 after:-left-8 after:bg-ternary after:rounded-full"

const showAnimation = ref(true)
const iconColor = ref('D652E9')

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

    <div id="1" class="text-white flex flex-col-reverse gap-4 pt-10 justify-center h-dvh snap-center relative items-center 
        sm:flex-col sm:flex-col-reverse sm:items-center sm:p-10
        md:flex-col md:flex-col-reverse md:items-center md:p-10
        lg:items-start lg:flex-row lg:pt-30"
        :class="[{'motion-preset-fade' :  showAnimation}] ">
        <div class="w-fit sm:w-fit md:w-fit lg:w-xl pt-7 flex flex-col gap-8 ">
            <p class="text-lg sm:text-lg md:text-lg lg:text-2xl font-bold">Hey, I'm <span class="italic text-ternary">Rencell</span></p>

            <div class="text-sm sm:text-sm md:text-sm lg:text-[1rem] xl:text-lg">
                I'm Rencell Tobelonia, currently studying Information Technology at Cavite State University - Bacoor. Technology excites me 
                every time I encounter something to solve or bugs to fix. Since I was a kid, I was crazily interested in hacking; this idea drives me to pursue this career path.
            </div>

            <div class="w-full sm:w-sm">
                <div class="grid grid-cols-7 sm:grid-cols-5 gap-4 motion-preset-focus ">
                    <div class="p-3 rounded-full bg-primary w-10 sm:w-fit">
                        <img class="w-5 sm:w-5 md:w-6 lg:w-6 xl:w-8" :src="'https://cdn.simpleicons.org/html5/' + iconColor" />
                    </div>
                    <div class="p-3 rounded-full bg-primary w-10 sm:w-fit">
                        <img class="w-5 sm:w-5 md:w-6 lg:w-6 xl:w-8" :src="'https://cdn.simpleicons.org/css/' + iconColor" />
                    </div>
                    <div class="p-3 rounded-full bg-primary w-10 sm:w-fit">
                        <img class="w-5 sm:w-5 md:w-6 lg:w-6 xl:w-8" :src="'https://cdn.simpleicons.org/javascript/' + iconColor" />
                    </div>
                    <div class="p-3 rounded-full bg-primary w-10 sm:w-fit">
                        <img class="w-5 sm:w-5 md:w-6 lg:w-6 xl:w-8" :src="'https://cdn.simpleicons.org/Python/' + iconColor" />
                    </div>
                    <div class="p-3 rounded-full bg-primary w-10 sm:w-fit">
                        <img class="w-5 sm:w-5 md:w-6 lg:w-6 xl:w-8" :src="'https://cdn.simpleicons.org/tailwindcss/' + iconColor" />
                    </div>
                    <div class="p-3 rounded-full bg-primary w-10 sm:w-fit">
                        <img class="w-5 sm:w-5 md:w-6 lg:w-6 xl:w-8" :src="'https://cdn.simpleicons.org/bootstrap/' + iconColor" />
                    </div>
                    <div class="p-3 rounded-full bg-primary w-10 sm:w-fit">
                        <img class="w-5 sm:w-5 md:w-6 lg:w-6 xl:w-8" :src="'https://cdn.simpleicons.org/php/' + iconColor" />
                    </div>
                    <div class="p-3 rounded-full bg-primary w-10 sm:w-fit">
                        <img class="w-5 sm:w-5 md:w-6 lg:w-6 xl:w-8" :src="'https://cdn.simpleicons.org/vuedotjs/' + iconColor" />
                    </div>
                </div>
            </div>
        </div>

        <div class="w-32 sm:w-32 md:w-32 lg:w-64"> 
            <img class="w-full rounded-full" src="../../assets/media/profile.png" alt="">
        </div>

        <i class="bi bi-chevron-double-down absolute text-xl sm:text-4xl h-fit text-ternary bottom-5 motion-preset-oscillate "></i>
    </div>

    <div id="2" class="w-full h-dvh snap-center ">

        <div class="grid grid-auto-fit w-full gap-0 sm:gap-10 gap-y-5 pt-5 sm:pt-5 md:pt-10 lg:pt-10">
            <div >
                <p class="text-4xl font-bold text-white pb-10 w-fit">Education</p>
                <div class="border-l-2 ps-6 border-primary flex flex-col gap-4 text-sm sm:text-sm md:text-base">
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
            <div >
                <p class="text-4xl font-bold text-white pb-10">Work</p>
                <div class="border-l-2 ps-6 border-primary flex flex-col gap-4">
                    <div class="text-white bg-primary rounded-3xl p-3   relative flex flex-col gap-1"
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
