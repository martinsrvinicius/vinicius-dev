<template>
    <div class="card-container">
        <va-collapse>
            <template #header>
                <div class="header">
                    <img :src="ImgPath" alt="">
                    <p>{{ props.item.text }}</p>
                </div>
            </template>

            <template #body>
                <div class="content">

                    <va-rating class="rating" v-model="value" color="#ffff"  :size="25"  disabled 
                    />
                <span>{{ props.item.description }}</span>
                </div>
            </template>
        </va-collapse>
    </div>
</template>


<script setup lang="ts">
import { computed, ref } from 'vue';
const props = defineProps(['item'])
const value = ref(props.item.rate)
const ImgPath = computed(() => {
    const path = new URL(`../../assets/${props.item.name}.svg`, import.meta.url).href;
    return path
});






</script>

<style scoped>
.card-container {
    margin-bottom: 100px;
    width: 200px;
    height: fit-content;
}

.card-container:hover {
    filter: drop-shadow(0 0 2em #42b883aa);
    cursor: pointer;
}

.col-body {
    width: 50px;
}

.header {
    display: flex;
    flex-direction: column;
    height: 190px;
    background-color: #34353a;
    align-items: center;
    padding-top: 5px;
    border-radius: 10px;
}

.content {
    color: rgb(35, 35, 35);
    background-color: gray;
    height: 160px;
    overflow-y: auto;
    margin: auto;
    font-size: 1rem;
}

img {
    margin-top: auto;
    width: 100px;
}

.rating {
    margin: auto;
    display: flex;
    justify-content: center;
    margin-top: 20px;
    margin-bottom: 10px;
}

span {
    text-align: justify;
    text-justify: inter-word;
    margin:4px;
}
</style>