<script setup>


</script>

<template>

    <div class="grid grid-cols-12 gap-4 text-white motion-preset-fade  ">
        <div class="flex flex-col gap-4 col-span-6">
            <p class="text-4xl font-bold">Hello, Welcome</p>
            <p class="text-2xl font-bold bg-ternary w-fit px-2 motion-preset-bounce ">My Portfolio</p>
            <div class="flex gap-4">
                <div class="bg-primary p-2 rounded-xl text-xl font-bold grow motion-preset-slide-right  motion-duration-600">
                    <p>Total Projects</p>
                    <p class="text-center text-5xl p-4">7</p>
                </div>
                <div class="bg-primary p-2 rounded-xl text-xl font-bold grow motion-preset-slide-right  motion-duration-800">
                    <p>Ongoing Projects</p>
                    <p class="text-center text-5xl p-4">0</p>
                </div>
            </div>
        </div>
        <div class="col-span-6 bg-primary rounded-xl p-4 motion-preset-slide-right  motion-duration-900">
            <p class="font-bold pb-6 text-xl">About</p>
            <p class="text-overflow-ellipsis text-lg">&emsp;&emsp;Hello, I'm a programmer solely focused on backend development and somewhat involved in web designing. My goal for every project is to learn something new, and the knowledge gained contributes to my continuous self-improvement.</p>
        </div>
        <div class="col-span-6 bg-primary rounded-xl p-4 motion-preset-slide-right  motion-duration-600">
            <p class="font-bold pb-6 text-xl">Project preview</p>
            <div class="w-full flex justify-center ">
                <div class="w-52 ">

                    <img class="w-full" src="../../assets/media/profile.png" alt="">
                </div>
            </div>

        </div>
        <div class="col-span-6 flex flex-col gap-4">
            
            <div class=" bg-primary rounded-xl grow p-4 motion-preset-slide-right  motion-duration-800">
                <p class="font-bold pb-6 text-xl">Skillset</p>
            </div>
            <div class=" bg-primary rounded-xl grow p-4 motion-preset-slide-right  motion-duration-800">
                <p class="font-bold pb-6 text-xl">Contact</p>
            </div>


        </div>
    </div>

</template>

<style scoped></style>
