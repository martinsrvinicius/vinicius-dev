<template>
    <div class="main">
        <h1>Experience</h1>

        <section v-for="item in items" :key="item.company">
            <ExperienceCard :item="item" style="margin:30px 0px" />
        </section>

    </div>
</template>

<script setup lang="ts">
import ExperienceCard from './ExperienceCard.vue'
import { ref } from 'vue'

const items = ref([
    {
        company: 'Discurso Virtual',
        url: 'https://dv-ti.com',
        year: '2023',
        location: 'Guimarães, Portugal',
        description: 'Discurso Virtual is a Portuguese company specialized in management and  billing software such as PHC and Sage. It also carries out software programming for its customers on demand. Most projects are made in Vue 3 and PHP.',
        role: 'Fullstack Vue & PHP',
        tech: ['Vue 3', 'PHP', 'Worpress'],
        current: 'Current'
    },
    {
        company: 'IOTAG',
        url: 'https://www.iotag.com.br/',
        year: '2022',
        location: 'Curitiba, Brasil',
        description: 'IOTAG is a Brazilian startup that has been revolutionizing the market with its telemetry devices for agribusiness machinery. My main functions at the beginning of our partnership were to act as a front-end developer working in the maintenance of web platforms using the VUE.js framework. A second challenge embraced by me was the maintenance and development of new functionalities in the mobile application. I developed new skills in Android Studio and Java',
        role: 'Frontend Vue & Java Android',
        tech: ['Vue 2', 'Java', 'Android'],
        current: null
    },

])

</script>

<style scoped>
.main {
    background-color: #34353a;
}

h1 {
    text-align: start;
    margin-left: 10%;
    position: relative;
    bottom: 23px;
}
</style>