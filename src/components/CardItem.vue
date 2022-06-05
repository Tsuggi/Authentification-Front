<template>
    <div class="w-72 max-w-full border border-gray-300 rounded-sm bg-white" v-if="name.last && name.first && email.email && location.country">
        <div class="p-6">
            <h5 class="text-lg font-bold"> {{ name.last + " " + name.first }} </h5>
            <h5 class="text-lg font-medium"> {{ email.email }} </h5>
            <h5 class="text-lg font-medium">Pays : {{ location.country }}</h5>
        </div>
    </div>

    <div class="w-72 max-w-full border border-gray-300 rounded-sm bg-white flex justify-center items-center" v-else>
        <SpinIconVue />
    </div>
</template>

<script setup>
import { ref } from 'vue';
import SpinIconVue from './Icones/SpinIcon.vue';

const name = ref({})
const email = ref({})
const location = ref({})

const URL_API = "https://randomuser.me/api/"
fetch(URL_API)
    .then(response => response.json())
    .then(data => {
        name.value = data.results[0].name
        email.value = data.results[0]
        location.value = data.results[0].location
    })
    .catch(error => "error API randomUser : " + error)

</script>

<style scoped>
</style>