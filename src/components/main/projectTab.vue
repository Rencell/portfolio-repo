<script setup>
import proj_component from '../../components/main/projectComponent/component.vue'
</script>

<template>

    <div>
        <p class="text-2xl font-bold text-white pb-5">My Projects</p>
        <div class="grid grid-cols-12 gap-5">
            <proj_component :name="'Attendance System With RFID & E-MAIL'" :date="'June 22 2022'">
                <img class="rounded-t-2xl" src="../../assets/Projects/RFID.png" alt="">
            </proj_component>

            <proj_component :name="'Point Of Sale | Milktea'" :date="'Apr 5, 2022'">
                <img class="rounded-t-2xl" src="../../assets/Projects/RFID.png" alt="">
            </proj_component>

            <proj_component :name="'Point Of Sale | Plants'" :date="'Dec 17, 2021'">
                <img class="rounded-t-2xl" src="../../assets/Projects/RFID.png" alt="">
            </proj_component>

            <proj_component :name="'Snake Game'" :date="'July 8, 2023'">
                <img class="rounded-t-2xl" src="../../assets/Projects/RFID.png" alt="">
            </proj_component>

            <proj_component :name="'Gem Odyssey Game'" :date="'January 15, 2024'">
                <img class="rounded-t-2xl" src="../../assets/Projects/RFID.png" alt="">
            </proj_component>

            <proj_component :name="'Payroll System'" :date="'January 20, 2024'">
                <img class="rounded-t-2xl" src="../../assets/Projects/RFID.png" alt="">
            </proj_component>
            
            <proj_component :name="'RFID Student Attendance System'" :date="'September 04, 2024'">
                <img class="rounded-t-2xl" src="../../assets/Projects/RFID.png" alt="">
            </proj_component>
        </div>
    </div>

</template>

<style scoped></style>
