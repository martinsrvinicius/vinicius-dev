<template>
    <div class="main">
        <h1>Academic Record</h1>

        <section v-for="item in items" :key="item.company">
            <AcademicRecordCard :item="item" style="margin:30px 0px"/>
        </section>
    
    </div>
</template>

<script setup lang="ts">
import AcademicRecordCard from './AcademicRecordCard.vue'
import {ref} from'vue'

const items = ref([
    {
        company:'UNINTER - Universidade Internacional',
        url:'https://www.uninter.com/',
        year:'2022 - 2025',
        location:'',
        role:'Software Engineering',
        description:'Engineering Undergraduate Course',
        tech: ['Engineering'],
        current:''
    },
    {
        company:'PHC - Developer Partner',
        url:'https://phcgo.net/developers/',
        year:'2023',
        location:'',
        role:'Software Development',
        description:'',
        tech: ['Certification', '12 hours'],
        current:''
    },
    {
        company:'Udemy - Maxmilian Schwarzmüller',
        url:'https://www.udemy.com/course/vuejs-2-the-complete-guide/',
        year:'2022',
        role:'Software Development',
        location:'',
        description:'Vue - The Complete Guide (incl. Router & Composition API)',
        tech: ['Vue 2', 'Vue 3'],
        current:null
    },
    {
        company:'Bootcamp Full Stack - DevSuperior',
        url:'https://devsuperior.com.br/',
        year:'2022',
        role:'Software Development',
        location:'',
        description:'Java with Spring Boot and ReactJS',
        tech: ['Java', 'Spring Boot', 'ReactJS'],
        current:null
    },
    {
        company:'Prof. Gustavo Guanabara',
        url:'https://www.cursoemvideo.com/',
        year:'2021',
        role:'Software Development',
        location:'',
        description:'Javascript and MySQL Database',
        tech: ['Javascript', 'MySQL'],
        current:null
    },
    {
        company:'Udemy - Prof. Nélio Alves',
        url:'https://www.udemy.com/user/nelio-alves/',
        year:'2021',
        role:'Software Development',
        location:'',
        description:'Complete Java, Object Oriented Programming, Programming Algorithm and Logic, C Language and Python',
        tech: ['Java', 'OOP', 'Algorithm', 'Logic', 'C', 'Python'],
        current:null
    },
    {
        company:'Udemy - Conexão Agile ',
        url:'https://www.udemy.com/user/julio-mesquita/',
        year:'2021',
        role:'Scrum',
        location:'',
        description:'The Scrum Fundamentals',
        tech: ['Java', 'OOP', 'Algorithm', 'Logic', 'C', 'Python'],
        current:null
    },
 
])

</script>

<style scoped>
.main {
    background-color: #34353a;
}   
h1{
    text-align:start;
    margin-left:10%;
    position:relative;
    bottom:23px;
} 
</style>