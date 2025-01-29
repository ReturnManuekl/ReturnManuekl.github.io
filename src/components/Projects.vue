<template>
    <section>
        <h1 id="pro">Projects</h1>
        <Project v-for="(elm, index) in projects" :key="index" :value="elm" />
    </section>
</template>

<script setup>
    import Project from './Project.vue'

    let projects = [
        {
            title: 'Sac-visa',
            img: '/img/sacvisa1.jpg',
            text: 'I developed an informative and attractive website about hydraulic concrete, highlighting the properties, applications, and advantages of this material. Serving as a resource for both construction professionals and customers interested in purchasing concrete products.',
            live: 'https://www.sacvisa.com.mx/',
        },
        {
            title: 'Ledezma y abogados',
            img: '/img/abogados.JPG',
            text: 'I developed a professional and attractive website for a law firm, which would serve as an information platform for potential and current clients. It reflected the seriousness and experience of the firm, as well as facilitated contact and navigation.',
            live: 'https://ledezmayabogados.com.mx/nosotros-expertos-en-propiedad-intelectual/',
        },
        {
            title: 'Sports Forecaster',
            img: '/img/sport1.jpg',
            text: 'I developed an interactive and dynamic web application that provides hockey fans with a complete guide to NHL draft day. The platform includes information on strategies, players to watch, and tips to maximize the draft experience. Participating primarily in the Front end with Vue.js',
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