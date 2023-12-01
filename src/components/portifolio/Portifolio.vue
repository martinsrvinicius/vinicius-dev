<template>
    <section>
        <h1>Portifolio</h1>
        <div class="skills-card-container">
            <div v-for="item in skills" :key="item.id">
                <PortifolioCard class="inner-skills-container" :item="item" />
            </div>
        </div>
    </section>
</template>

<script setup lang="ts">
import PortifolioCard from './PortifolioCard.vue'
import { ref } from 'vue'
const skills = ref([
    {
        id: 1,
        name: 'rosemeri.png',
        text: 'Rosemeri Beauty',
        description: 'System built in Vue and PHP that allows scheduling, confirmation of appointments and cancellation of beauty services.',
        link:'https://rosemeri-beauty.vercel.app/'
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

