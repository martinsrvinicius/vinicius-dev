<template>
    <div class="page">
        <section class=" top-container">
            <div class="navbar">
                <Navbar />
            </div>

            <div class="top-flex">
                <div class=" left">
                    <div class="inner-left">
                        <p class="name-container">I'M <strong class="name"> Vinícius Martins </strong>
                        </p>
                        <p style="position: relative;bottom:10px">Fullstack Developer
                        </p>
                    </div>
                    <va-button preset="plain">
                        <p class="btn-contact">
                            Contact Me
                        </p>
                    </va-button>
                </div>
                <div class="right">
                    <va-avatar size="350px">
                        <img class="img-profile" src="../assets/foto-perfil.jpg" alt="">
                    </va-avatar>

                    <!--SOCIAL MEDIA-->
                    <div class="social-container" style="display: none;">
                        <div class="item-social">
                            <img class="img-social" src="../assets/linkedin.svg
                        " alt="">
                            <span>Vinicius R. Martins</span>
                        </div>
                        <div class="item-social">
                            <img class="img-social" src="../assets/github.svg
                        " alt="">
                            <span>martinsrvinicius</span>
                        </div>
                        <div class="item-social">
                            <img class="img-social" src="../assets/whatsapp.svg
                        " alt="">
                            <span>(+351) 962 468 873</span>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <section>
            <About />
        </section>

        <section>
            <MySkills />
        </section>

        <section style="margin-top: 100px;">
            <Portifolio />
        </section>

        <section style="margin-top: 100px;">
            <Experience />
        </section>
    </div>
</template>

<script setup lang="ts">
import Navbar from '../components/navbar/Navbar.vue'
import About  from '../components/about/About.vue'
import MySkills  from '../components/skills/MySkills.vue'
import Portifolio  from '../components/portifolio/Portifolio.vue'
import Experience  from '../components/experience/Experience.vue'

</script>

<style scoped>
.page {
    display: flex;
    flex-direction: column;
    user-select: none;
    overflow: auto;
}

.top-container {
    display: flex;
    flex-direction: column;
    background-color: #34353a;
    height: 650px;
    margin: auto;
    width: 100vw;
    overflow: hidden;
    box-shadow: -2px 14px 24px -14px rgba(0, 0, 0, 0.75);
    -webkit-box-shadow: -2px 14px 24px -14px rgba(0, 0, 0, 0.75);
    -moz-box-shadow: -2px 14px 24px -14px rgba(0, 0, 0, 0.75);
}

.img-profile {

    filter: grayscale(90%);
}

p {
    color: white
}

.name {
    color: #ffc86b;
    font-size: 3.5rem;
}

.social-container {
    display: flex;
    flex-direction: column;
    text-align: center;
    justify-content: space-evenly;
}

.navbar {}

.top-flex {
    display: flex;
}

.left {
    width: 70%;
    font-size: 30px;
}

.left>span {
    margin-top: 50%;
}

.name-container {
    margin-top: 15%;
}

.item-social {
    height: 40px;
    display: flex;

}

.item-social>span {
    padding-top: 8px;
}

.img-social {
    width: 25px;
    margin-right: 10px;
}

.img-container {
    border-radius: 5px;
    border: 1px solid;
}

.btn-contact {
    border: 1px solid #ffc86b;
    width: 150px;
    height: 50px;
    display: flex;
    border-radius: 5px;
    align-items: center;
    justify-content: center;
}

.inner-left {
    width: 70%;
    margin: auto;
}
</style>