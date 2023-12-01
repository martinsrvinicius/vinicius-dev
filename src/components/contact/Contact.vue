<template>
    <div class="container">
        <div class="top">
            <div class="empty"></div>
            <h1>Contact Me</h1>
            <div class="empty"></div>
        </div>
        <div class="inner-container">
            <div class="item">
                <img src="../../assets/email.svg" />
                <p><a href="mailto:martinsrvinicius@gmail.com">vinim.dev@gmail.com</a></p>
            </div>

            <div class="item">
                <img src="../../assets/phone.svg" />
                <p><a href="tel:+351-962-468-873">(+351) 962 468 873</a></p>
            </div>
        </div>

        <div class="bottom">
            <div class="empty-bottom"></div>
            <div class="social">
                <SocialMedia />
            </div>
            <div class="empty-bottom"></div>
        </div>
    </div>
</template>

<script setup lang="ts">
import SocialMedia from '../social/SocialMedia.vue'

</script>

<style scoped>
.container {
    background-color: #3d3e42;
    padding-bottom: 0px;
}

.inner-container {
    width: 100%;
    margin: auto;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-around;
}



.item {
    display: flex;
    align-items: center;
    padding: 10px;
    height: 30px;
    width: 250px;
    border-radius: 5px;
    background-color: #242424;
    margin-bottom: 10px;
}



img {
    width: 25px;
    margin-right: 10px;
}

a {
    color: #ffc86b;
}

.top {
    display: flex;
    justify-content: space-evenly;
    height: 90px;
}


.empty {
    border-top: 1px solid #ffc86b;
    min-width: 23%;
}



h1 {
    width: 62%;
    position: relative;
    bottom: 50px;
}

.bottom {
    margin-top: 50px;
    display: flex;
    justify-content: space-evenly;
}

.empty-bottom {
    border-bottom: 1px solid #ffc86b;
    min-width: 23%;
}



.social {
    width: 62%;
    position: relative;
    top: 25px;
}

@media screen and (min-width: 450px) {
    .empty-bottom {
        min-width: 38%;
    }

    .empty {
        min-width: 38%;
    }

    .inner-container {
        width: 550px;
        flex-direction: row;
    }
}
</style>