<template>
    <!--SOCIAL MEDIA-->
    <div class="social-container">
        <div class="item-social">
            <a href="https://www.linkedin.com/in/vinicius-r-martins-98129074/" target="_blank">
                <img class="img-social" src="../../assets/linkedin.svg
                        " alt="">
            </a>
        </div>
        <div class="item-social">
            <a href="https://github.com/martinsrvinicius" target="_blank">
                <img class="img-social" src="../../assets/github.svg
                        " alt="">
            </a>
        </div>
        <div class="item-social">
            <a href="https://wa.me/message/PJF4E5AT7BH2F1" target="_blank">
                <img class="img-social" src="../../assets/whatsapp.svg
                        " alt="">
            </a>
        </div>
    </div>
</template>

<style scoped>
.social-container {
    display: flex;
    text-align: center;
    justify-content: space-around;
    max-width: 600px;
}

.item-social {
    height: 40px;
    display: flex;
    justify-content: center;
}

.item-social>span {
    padding-top: 8px;
}

.img-social {
    width: 25px;
    margin-right: 0px;
}

span {
    font-size: 1rem;
}

@media screen and (min-width: 450px) {
    .social-container {
    display: flex;
    text-align: center;
    justify-content: space-evenly;
    max-width: 600px;
}
.img-social {
    width: 25px;
    margin-right: 0px;
}
}
</style>