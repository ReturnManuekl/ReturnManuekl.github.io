<template>
    <section>
        <h1 id="pro">Proyectos</h1>
        <Project v-for="(elm, index) in projects" :key="index" :value="elm" />
    </section>
</template>

<script setup>
    import Project from './Project.vue'

    let projects = [
        {
            title: 'Sac-visa',
            img: '/img/sacvisa.jpg',
            text: 'Desarrolle un sitio web informativo y atractivo sobre concretos hidráulicos, destacando las propiedades, aplicaciones y ventajas de este material. Sirviendo como un recurso tanto para profesionales de la construcción como para clientes interesados en adquirir productos de concreto.',
            live: 'https://www.sacvisa.com.mx/',
        },
        {
            title: 'Ledezma y abogados',
            img: '/img/abogados.jpg',
            text: 'Desarrolle una página web profesional y atractiva para un bufete de abogados, que sirviera como plataforma informativa para clientes potenciales y actuales. Reflejar la seriedad y la experiencia del bufete, así como facilitar el contacto y la navegación.',
            live: 'https://ledezmayabogados.com.mx/nosotros-expertos-en-propiedad-intelectual/',
        },
        {
            title: 'Sports Forecaster',
            img: '/img/sport.jpg',
            text: 'Desarrolle una aplicación web interactiva y dinámica que proporcione a los fanáticos del hockey una guía completa sobre el día del draft de la NHL. La plataforma incluye información sobre estrategias, jugadores a seguir, y consejos para maximizar la experiencia del draft. Particimando principalmente en el Front endParticipación principalmente en el front end con Vue.js',
            live: 'https://sportsforecaster.com/',
        },
    ]
</script>

<style scoped>
    h1 {
        font-size: 48px;
        font-weight: 600;
        text-align: center;
        margin: 100px 0 100px 0;
        padding-top: 100px;
    }

    @media screen and (max-width: 715px) {
        h1 {
            font-size: 35px;
        }
    }

</style>