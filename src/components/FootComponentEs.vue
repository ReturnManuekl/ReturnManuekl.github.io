<template>
    <div class="caja-foot">
        <h1>Contactame!</h1>
        <div>
            <img class="icono-correo" src="/img/icono-correo.png" alt="">
            <a href="mailto: manuel.zerg@gmail.com">manuel.zerg@gmail.com</a>
            <img class="icono-in" src="/img/iconoIn.png"  alt="">
            <a target="_blank" href="https://www.linkedin.com/in/manuekl/">LinkedIn</a>
        </div>
        <p>Made by Manuel Alcantar © 2024</p>
    </div>
</template>

<script setup>
</script>

<style scoped>
    .caja-foot {
        display: flex;
        flex-direction: column;
        align-items: center;
        margin-top: 200px;
    }

    .caja-foot > div {
        display: flex;
        align-items: center;
        margin-top: 25px;
    }

    h1 {
        font-size: 48px;
        font-weight: 600;
    }

    a {
        font-size: 16px;
    }


    a:hover {
        color: gray;
    }

    img {
        width: 25px;
    }

    .icono-correo {
        width: 33px;
    }

    .icono-in {
        margin-left: 15px;
    }

    p {
        font-size: 14px;
        margin-top: 25px;
        color: gray;
    }

    @media screen and (max-width: 715px) {
        h1 {
            font-size: 35px;
        }

        img {
            width: 19px;
        }

        .icono-correo {
            width: 22px;
        }

        a {
            font-size: 14px;
        }
    }
</style>