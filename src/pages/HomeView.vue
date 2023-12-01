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
                        <p style="position: relative;bottom:10px;">Fullstack Developer
                        </p>
                    </div>
                    <va-button preset="plain" href="#contact">
                        <p class="btn-contact">
                            Contact Me
                        </p>
                    </va-button>
                </div>
                <div class="right">
                    <va-avatar :size="size" class="avatar">
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

        <section id="about" >
            <About />
        </section>

        <section>
            <MySkills />
        </section>

        <section style="margin-top: 100px;" id="portifolio">
            <Portifolio />
        </section>

        <section style="margin-top: 100px;">
            <Experience />
        </section>

        <section style="margin-top: 100px;">
            <AcademicRecord />
        </section>

        <section style="margin-top: 100px;margin-bottom:30px; " id="contact">
            <Contact />
        </section>

        <section>
            <p class="bye">"Thanks for scrolling"</p>
        </section>

    </div>
</template>

<script setup lang="ts">
import Navbar from '../components/navbar/Navbar.vue'
import About from '../components/about/About.vue'
import MySkills from '../components/skills/MySkills.vue'
import Portifolio from '../components/portifolio/Portifolio.vue'
import Experience from '../components/experience/Experience.vue'
import AcademicRecord from '../components/academic/AcademicRecord.vue'
import Contact from '../components/contact/Contact.vue'
import { ref, onMounted } from 'vue'

const size = ref()
onMounted(() => {
    if (window.innerWidth > 400) {
        size.value = '350px'
    } else {
        size.value = '240px'
    }
})


</script>

<style scoped>
.page {
    display: flex;
    justify-content: center;
    flex-direction: column;
    user-select: none;
}

.top-container {
    display: flex;
    flex-direction: column;
    background-color: #34353a;
    height: fit-content;
    margin: auto;
    overflow: hidden;
}

.top-flex {
    display: flex;
    flex-direction: column;
    justify-content: center;
}

.left {
    font-size: 30px;
}

.name-container {
    margin-top: 15%;
}

.name {
    color: #ffc86b;
    font-size: 3.5rem;
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

p {
    color: white
}

.img-profile {
    filter: grayscale(90%);
}

.avatar {
    margin-top: 20px;
}

.right {
    margin-bottom: 40px;
}
.bye {
        color: #ffc86b;
        font-size: 1.5rem;
    }
@media screen and (min-width: 400px) {
    .page {
        display: flex;
        flex-direction: column;
        user-select: none;
        overflow: auto;
    }

    .top-container {
        height: 650px;
        margin: auto;
        width: 100vw;
        overflow: hidden;
        box-shadow: -2px 14px 24px -14px rgba(0, 0, 0, 0.75);
        -webkit-box-shadow: -2px 14px 24px -14px rgba(0, 0, 0, 0.75);
        -moz-box-shadow: -2px 14px 24px -14px rgba(0, 0, 0, 0.75);
    }



    .social-container {
        display: flex;
        flex-direction: column;
        text-align: center;
        justify-content: space-evenly;
    }

    .top-flex {
        display: flex;
        flex-direction: row;
        min-width: 90%;
        margin: 0px auto;
    }

    .left {
        width: 65%;
        font-size: 30px;
    }

    .left>span {
        margin-top: 50%;
    }

    .right {
        margin-right: 20px;
    }

    .avatar {
        margin-top: 50px;
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

    
}
</style>