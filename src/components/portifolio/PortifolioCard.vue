<template>
    <div class="card-container">
        <div class="header" @mouseenter="isHover = true"  @mouseleave="isHover = false">
            <div  :class="[isHover ? 'show':'hide']" >
                <p>{{ props.item.text }}</p>
                <p>{{props.item.description}}</p>
                <va-button preset="plain" >
                    <a target="_blank" href="https://rosemeri-beauty.vercel.app/"><p class="btn-link">See more</p></a>
                </va-button>
            </div>
            <div class="img-position" :class="[!isHover ? 'img-container':'img-container2']">
                <img :src="ImgPath" alt="Imagem">
                <p>{{ props.item.text }}</p>
            </div>
        </div>
    </div>
</template>


<script setup lang="ts">
import { computed, ref } from 'vue';
const props = defineProps(['item'])
const isHover = ref()
const ImgPath = computed(() => {
    const path = new URL(`../../assets/${props.item.name}`, import.meta.url).href;
    return path
});



</script>

<style scoped>
.card-container {
    margin-bottom: 100px;
    width: 350px;
    height: fit-content;
    transition: .4s ease-in-out;
}

.card-container:hover {
    filter: drop-shadow(0 0 2em #42b883aa);
    cursor: pointer;
    transition: .4s ease-in-out;

}

.col-body {
    width: 50px;
}

.header {
    display: flex;
    flex-direction: column;
    height: 350px;
    background-color: #34353a;
    align-items: center;
    padding-top: 5px;
    border-radius: 10px;
    max-width: 100%;
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
    width: 100%;
    height: 100%;
    object-fit: contain;
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
    margin: 4px;
}

.hide {
    opacity: 0;
    transform: translateY(0);
    transition: .4s ease-in-out;
}

.show {
    height: 500px;
    width: 300px;
    opacity: 1;
    transition: .4s ease-in-out;
    transform: translateY(30%);
}

.img-container {
    transform: opacity(1);
    transition: .4s ease-in-out;
}

.img-container2 {
    opacity: 0;
    transition: .4s ease-in-out;
}

.props {
    height: 500px;
    width: 300px;
    opacity: 1;
    transition: .4s ease-in-out;
    transform: translateY(100);
}

.props-down {
    height: 500px;
    width: 300px;
    opacity: 0;
    transition: .4s ease-in-out;
    transform: translateY(0);
}

.btn-link {
    color: #ffc86b;
    border: 1px solid #ffc86b;
    width: 150px;
    height: 50px;
    display: flex;
    align-items: center;
    justify-content: center;
    border-radius: 5px;
}

.img-position {
    position: relative;
    bottom: 200px;
}

@media screen and(min-width: 400px){
    .card-container {
    margin-bottom: 100px;
    width: 350px;
    height: fit-content;
    transition: .4s ease-in-out;
}

.card-container:hover {
    filter: drop-shadow(0 0 2em #42b883aa);
    cursor: pointer;
    transition: .4s ease-in-out;
}

.col-body {
    width: 50px;
}

.header {
    display: flex;
    flex-direction: column;
    height: 350px;
    background-color: #34353a;
    align-items: center;
    padding-top: 5px;
    border-radius: 10px;
    max-width: 100%;
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
    width: 200px;
    height: 200px;
    object-fit: cover;
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
    margin: 4px;
}

.hide {
    opacity: 0;
    transform: translateY(0);
    transition: .4s ease-in-out;
}

.show {
    height: 500px;
    width: 300px;
    opacity: 1;
    transition: .4s ease-in-out;
    transform: translateY(30%);
}

.img-container {
    transform: opacity(1);
    transition: .4s ease-in-out;
}

.img-container2 {
    opacity: 0;
    transition: .4s ease-in-out;
}

.props {
    height: 500px;
    width: 300px;
    opacity: 1;
    transition: .4s ease-in-out;
    transform: translateY(100);
}

.props-down {
    height: 500px;
    width: 300px;
    opacity: 0;
    transition: .4s ease-in-out;
    transform: translateY(0);
}

.btn-link {
    color: #ffc86b;
    border: 1px solid #ffc86b;
    width: 150px;
    height: 50px;
    display: flex;
    align-items: center;
    justify-content: center;
    border-radius: 5px;
}

.img-position {
    position: relative;
    bottom: 100px;
}
}
</style>