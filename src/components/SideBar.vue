<template>
    <!-- To open on mobile, remove -translate-x-full lg:translate-x-0 and add translate-x-0 -->
    <div
        class="w-72 max-w-full bg-indigo-600 h-screen flex flex-col text-white fixed lg:sticky top-0 transition-transform transform duration-500 ease -translate-x-full lg:translate-x-0">
        <div class="flex-1 mt-8">
            <div class="mt-6">
                <RouterLink to="/"
                    class="flex justify-between no-underline w-full px-8 py-3 text-sm hover:text-blue-300 border-l-4 border-transparent">
                    <div class="flex justify-center items-center gap-4">
                        <HomeIcon /><span>Home</span>
                    </div>
                </RouterLink>
                <RouterLink to="/login"
                    class="flex justify-between no-underline w-full px-8 py-3 border-l-4 border-transparent text-sm hover:text-blue-300">
                    <div class="flex justify-center items-center gap-4">
                        <LoginIcon /><span>Login</span>
                    </div>
                </RouterLink>
                <RouterLink to="/data"
                    class="flex justify-between no-underline w-full px-8 py-3 border-l-4 border-transparent text-sm hover:text-blue-300">
                    <div class="flex justify-center items-center gap-4">
                        <DataIcon /><span>Data</span>
                    </div>
                </RouterLink>
            </div>
        </div>
        <div class="flex px-8 py-6 items-center">
            <div class="relative rounded-full w-12 h-12">
                <img src="https://gustui.s3.amazonaws.com/avatar.png"
                    class="absolute left-0 top-0 w-full h-full rounded-full object-cover" />
            </div>
            <div class="flex-1 ml-4">
                <p class="font-medium leading-none">Sylvain REMENANT</p>
                <a href="#" class="mt-2 no-underline text-xs text-gray-300 leading-none flex items-center gap-2">
                    <SettingIcon /> <span>Edit Profile</span>
                </a>
            </div>
        </div>
    </div>
</template>

<script setup>
import LoginIcon from '../components/Icones/LoginIcon.vue'
import HomeIcon from '../components/Icones/HomeIcon.vue'
import SettingIcon from '../components/Icones/SettingIcon.vue'
import DataIcon from './Icones/DataIcon.vue';
</script>

<style scoped>
.router-link-active {
    @apply transition-colors duration-200 ease-in-out  bg-blue-900 border-blue-400 hover:text-white
}
</style>