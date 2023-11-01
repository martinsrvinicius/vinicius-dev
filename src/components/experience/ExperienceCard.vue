<template>
    <div class="main">
        <div class="top">
            <div class="year">
                {{$props.item.year}}
            </div>
            <div class="item-flex">
                <div class="golden"><img src="../../assets/golden.svg" alt=""></div>
                <div class=" title"><span>{{props.item.company}}</span><span v-if="props.item.current"> - ({{ props.item.current }})</span></div>
            </div>
        </div>

        <div class="container">
            <div class="year">
            </div>
            <div class="right">
                <p>
                    {{ props.item.role }} <br>
                   <span><a :href="props.item.url"> {{ props.item.url }}</a></span> - <span>{{ props.item.location }}</span>
                </p>
                <p>
                    {{ props.item.description }}
                </p>
                <p class="tech-container">
                    <span v-for="tech in props.item.tech" class="tech">
                        {{ tech }}
                    </span>
                </p>
            </div>
        </div>
    </div>
</template>

<script setup lang="ts">
const props = defineProps(['item'])

</script>

<style scoped>
.main {
    max-width: 1500px;
    margin: auto;
}

.top {
    display: flex;
    align-items: center;
}

.container {
    display: flex;
}

.year {
    display: flex;
    justify-content: end;
    padding-right: 30px;
    width: 20%;
   
}

.item-flex {
    display: flex;
    align-items: center;
}

.right {
    width: 60%;
    border-left: 1.3px solid rgb(229, 229, 229);
    text-align: justify;
    text-justify: inter-word;
    padding-left: 50px;
}

.title {
    font-size: 1.5rem;
    padding-left: 19px;
}

.golden {

    filter: drop-shadow(0 0 .5em #ffc86b);

}

img {
    width: 20px;
    padding-top: 5px;
    position: relative;
    right: 10px;
}

.tech-container {
    display: flex;
    flex-direction: row;
}

.tech {
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: .8rem;
    height: 30px;
    min-width:80px;
    border: 1px solid #ffc86b;
    border-radius: 20px;
    margin-right: 5px;
}

a {
    color: white;
}

a:hover {
    cursor: pointer;
}
</style>