<template>
    <div class="bar-nav">
        <ul>
            <li>
                <a href="#about">{{ about }}</a>              
            </li>
            <li><a href="#pro">{{ projects }}</a></li>
            <li><a href="#contact">{{ contact }}</a></li>
            <li class="language-botton">
                <div class="button-dual">
                    <button id="es" @click="esButton">ES</button>
                    <button id="en" @click="enButton">EN</button>
                </div>
            </li>
        </ul>
    </div>
</template>

<script setup>
    import { ref, defineEmits } from 'vue';
    
    const emit = defineEmits(['en', 'es'])
    const about = ref('Sobre mi')
    const projects = ref('Proyectos')
    const contact = ref('Contacto')
    const esButton = () => {
        about.value = 'Sobre mi'
        projects.value = 'Proyectos'
        contact.value = 'Contacto'
        emit("es")
    } 
    const enButton = () => {
        about.value = 'About'
        projects.value = 'Projects'
        contact.value = 'Contact'
        emit("en")
    } 
</script>

<style scoped>
    .bar-nav {
        color: black;
    }

    ul {
        display: flex;
        justify-content: end;
        gap: 2rem;
        list-style: none;
        font-size: 1.5rem;
    }

    a:hover {
        color: gray;
    }

    #idLanguage {
        height: 25px;
        background-color: #353535;
        color: white;
        border-radius: 5px;
        border: none;
        cursor: pointer;
    }

    .language-botton {
        display: flex;
        align-items: center;
    }

    .button-dual {
        background:#212531;
        background: linear-gradient(110deg, white 50%, #353535 50%);
        border-radius: 5px;
        border: 2px solid #353535;
        display: flex;
        align-items: center;
        padding: 5px 0 5px 0;
    }

    .button-dual button{
        background-color: transparent;
        border: none;
        cursor: pointer;
    }

    .button-dual #en{
        color: white;
    }

    .button-dual #es{
        color: white;
        color: #353535;
    }

    @media screen and (max-width: 715px) {
        ul {
            font-size: 1rem;
        }

        #idLanguage {
            height: 20px;
            font-size: 12px;
        }
    }

    @media screen and (max-width: 425px) {
        ul {
            font-size: 12px;
            gap: .5rem;
        }

        #idLanguage {
            height: 18px;
            font-size: 10px;
        }
    }
</style>