<script setup>
const relativeElipsis = "after:content-[' s'] after:p-2 after:absolute after:top-0 after:-left-8 after:bg-ternary after:rounded-full"
</script>

<template>

    <div class="text-white flex gap-4 pt-32 justify-center motion-preset-fade h-dvh snap-center relative">
        <div class="w-xl pt-7 flex flex-col gap-8">
            <p class="text-2xl font-bold">Hey, I'm <span class="italic text-ternary">Rencell</span></p>

            <div class="text-lg">
                I'm Rencell Tobelonia, currently studying Information Technology at Cavite State University. Computers
                excite me every time I encounter something to troubleshoot or bugs to fix. I'm deeply passionate about
                my course, having been immersed in the world of computers since I was a kid.
            </div>

            <div class="flex gap-4 motion-preset-focus ">
                <div class="p-2 rounded-full bg-primary w-fit">
                    <img src="../../assets/icons/Html.svg" alt="">
                </div>
                <div class="p-2 rounded-full bg-primary w-fit">
                    <img src="../../assets/icons/Html.svg" alt="">
                </div>
                <div class="p-2 rounded-full bg-primary w-fit">
                    <img src="../../assets/icons/Html.svg" alt="">
                </div>
            </div>
        </div>

        <div class="w-64"> <img class="w-full rounded-full" src="../../assets/media/profile.png" alt=""></div>

        <i class="bi bi-chevron-double-down absolute text-4xl h-fit text-ternary bottom-5 motion-preset-oscillate "></i>
    </div>

    <div class="w-full h-dvh snap-center ">

        <div class="grid grid-cols-12 gap-20
         pt-20">
            <div class="col-span-12 md:col-span-12 xl:col-span-6 ">
                <p class="text-4xl font-bold text-white pb-10">Education</p>
                <div class="border-l-2 ps-6 border-primary flex flex-col gap-4">
                    <div class="text-white bg-primary rounded-3xl p-3  relative flex flex-col gap-1 motion-preset-slide-right motion-duration-400"
                        :class="[relativeElipsis]">
                        <p class="font-bold text-ternary">Junior Highschool</p>
                        <p>2016-2020</p>
                        <p>• City of Bacoor National High School Springville</p>
                    </div>

                    <div class="text-white bg-primary rounded-3xl p-3  relative flex flex-col gap-1 motion-preset-slide-right motion-duration-500"
                        :class="[relativeElipsis]">
                        <p class="font-bold text-ternary">Junior Highschool</p>
                        <p>2020-2022</p>
                        <p>• Informatics College Imus Cavite</p>
                    </div>
                    <div class="text-white bg-primary rounded-3xl p-3  relative flex flex-col gap-1 motion-preset-slide-right motion-duration-600"
                        :class="[relativeElipsis]">
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
                        :class="[relativeElipsis]">
                        Empty
                    </div>
                </div>

            </div>
        </div>


    </div>
</template>

<style scoped></style>
