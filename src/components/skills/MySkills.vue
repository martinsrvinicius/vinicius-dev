<template>
    <section>
        <h1>My Skills</h1>
        <div class="skills-card-container">
            <div v-for="item in skills" :key="item.id">
                <MySkillsCard class="inner-skills-container" :item="item" />
            </div>
        </div>
    </section>
</template>

<script setup lang="ts">
import MySkillsCard from './MySkillsCard.vue'
import { ref } from 'vue'
const skills = ref([
    {
        id: 1,
        name: 'vue',
        text: 'Vue',
        rate: 4,
        description: 'Able to create CLI, Vite, CRUD, Router, Axios, Pinia projects, API Rest'
    },
    {
        id: 2,
        name: 'javascript',
        text: 'Javascript',
        rate: 3,
        description: 'Working on it: Vanilla e Jquery'

    },
    {
        id: 3,
        name: 'html',
        text: 'HTML',
        rate: 5,
        description: 'Confortable working with it'
    },
    {
        id: 4,
        name: 'css',
        text: 'CSS',
        rate: 5,
        description: 'Able to create mobile responsivity'
    },
    {
        id: 5,
        name: 'figma',
        text: 'Figma',
        rate: 4,
        description: 'Able to create prototypes'
    },
    {
        id: 6,
        name: 'java',
        text: 'Java',
        rate: 2,
        description: 'Working on it: DTO, CRUD, REST controllers, services, pagination'
    },
    {
        id: 7,
        name: 'kotlin',
        text: 'Kotlin',
        rate: 1,
        description: 'Working on it...'

    },
    {
        id: 8,
        name: 'c',
        text: 'C',
        rate: 2,
        description: 'Working on it...'
    },
    {
        id: 9,
        name: 'android',
        text: 'Android Studio',
        rate: 3,
        description: 'Working on it:Eventbus, xml, components'
    },
    {
        id: 10,
        name: 'python',
        text: 'Python',
        rate: 2,
        description: 'Working on it: tuplas, arrays, loops etc.'
    },

    {
        id: 11,
        name: 'mysql',
        text: 'MySQL',
        rate: 3,
        description:'Capable to create databases, queries on tables, data import and export on Workbench.'
    },
    {
        id: 12,
        name: 'photoshop',
        text: 'Photoshop',
        rate: 4,
        description:'Confortable working with it.'
    },
    {
        id: 13,
        name: 'php',
        text: 'PHP',
        rate: 3,
        description:'Able to work on queries and retrieve JSON.'
    },
    {
        id: 14,
        name: 'premiere',
        text: 'Adobe Premiere',
        rate: 4,
        description:'Confortable working with it.'
    },
    {
        id: 15,
        name: 'spring',
        text: 'Spring Framework',
        rate: 1,
        description:'Working on it...'
    },
    {
        id: 16,
        name: 'wordpress',
        text: 'Wordpress',
        rate: 4,
        description:'Confortable working with it'
    },
    {
        id: 17,
        name: 'git',
        text: 'Git',
        rate: 3,
        description:'Able to work on remote repository.'
    },
    {
        id: 18,
        name: 'ae',
        text: 'After Effects',
        rate: 3,
        description:'Confortable working with it.'
    },
])


</script>

<style scoped>
.skills-card-container {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    justify-content: space-evenly;
    width: 80vw;
    height: fit-content;
    margin: auto;
}

.skills-card-container:hover {
   


}

.inner-skills-container {
    margin: 10px 10px;

}
</style>

