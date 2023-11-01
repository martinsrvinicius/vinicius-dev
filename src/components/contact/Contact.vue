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
                <p><a href="mailto:martinsrvinicius@gmail.com">martinsrvinicius@gmail.com</a></p>
            </div>

            <div class=" item">
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

<script setup>
import SocialMedia from '../social/SocialMedia.vue'

</script>

<style scoped>
.container {
    background-color: #3d3e42;
    padding-bottom: 0px;
}

.inner-container {
    width: 550px;
    margin: auto;
    display: flex;
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
    background-color: #242424
}

img {
    width: 25px;
    margin-right: 10px;
}

a {
    color: #ffc86b;
}

.top {
    display:flex;
    justify-content:space-evenly;
}

.empty {
   border-top: 1px solid #ffc86b;
   min-width:38%;
}

h1 {
    width:62%;
    position:relative;
    bottom:50px;
}

.bottom {
    margin-top:50px;
    display:flex;
    justify-content:space-evenly;
}

.empty-bottom {
   border-bottom: 1px solid #ffc86b;
   min-width:38%;
}

.social {
    width:62%;
    position:relative;
    top:25px;
}
</style>