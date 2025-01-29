<script setup>
  import { ref } from 'vue';
  import NavComponent from './components/NavComponent.vue'
  import Projects from './components/Projects.vue'
  import FootComponent from './components/FootComponent.vue'
  import ProjectsEs from './components/ProjectsEs.vue';
  import FootComponentEs from './components/FootComponentEs.vue';
  const vali = ref(true);
  const saludo = ref('Hola, soy')
  const cv = ref('Descargar CV')
  const about = ref("Sobre mi")
  const infoCont = ref('Contacto')
  const textOne = ref("¡Hola! Soy Manuel, un desarrollador web de Zapopan, Jalisco, México. Me especializo en desarrollo front-end y me encanta desarrollar con cualquier herramienta que sea adecuada para el trabajo.")
  const TextTwo = ref("Fuera del trabajo, me encontrarás tocando la guitarra con mi banda, jugando videojuegos, jugando fútbol o cocinando mis comidas favoritas.")
  const skills = ref("Habilidades")
  const tec = ref("Herramientas y tecnologías")
  const esButton = () => {
    vali.value = true
    saludo.value = "Hola, soy"
    cv.value = "Descargar CV"
    about.value = "Sobre mi"
    infoCont.value = "Contacto"
    textOne.value = "¡Hola! Soy Manuel, un desarrollador web de Zapopan, Jalisco, México. Me especializo en desarrollo front-end y me encanta desarrollar con cualquier herramienta que sea adecuada para el trabajo."
    TextTwo.value = "Fuera del trabajo, me encontrarás tocando la guitarra con mi banda, jugando videojuegos, jugando fútbol o cocinando mis comidas favoritas."
    skills.value = "Habilidades"
    tec.value = "Herramientas y tecnologías"
  }
  const enButton = () => {
    vali.value = false
    saludo.value = "Hello, I'm"
    cv.value = "Download CV"
    about.value = "About me"
    infoCont.value = "Contact Info"
    textOne.value = "Hi! I'm Manuel, a Web Developer based in Zapopan, Jalisco, Mexico. I specialize in front-end development and love developing with whatever tools are right for the job."
    TextTwo.value = "Outside work, you will find me playing the guitar with my band, playing video games, playing football, or cooking my favorite foods."
    skills.value = "Skills"
    tec.value = "Tools and Technologies"
  }

  

</script>

<template>
  <header>
    <NavComponent @en="enButton" @es="esButton" />
  </header>

  <main>
    <section class="inicio">
      <div>
        <img class="perfil" src="/img/perfilEditada.jpg" alt="">
      </div>
      <div class="info-inicio">
        <p>{{ saludo }}</p>
        <h2>Manuel Alcantar</h2>
        <h3>Web developer</h3>
        <div class="btn-info">
          <a href="/archivos/cv_manuel_alcantar.pdf" download="cv_manuel_alcantar.pdf"><button class="cv">{{ cv }}</button></a>
          <a href="#contact"><button class="info">{{ infoCont }}</button></a>
        </div>
      </div>
    </section>
    <div class="about" id="about">
      <h2 class="title-about">{{ about }}</h2>
      <div class="about-info">
        <div class="about-text">
          <p>{{ textOne }}</p>
          <p>{{ TextTwo }}</p>
        </div>
        <div class="skills">
          <div class="subTitle-skills">
            <img src="/img/icono-dev.png" alt="">
            <h3>{{ skills }}</h3>
          </div>
          <button>HTML</button>
          <button>CSS</button>
          <button>JavaScript</button>
          <button>PHP</button>
          <button>SQL</button>
          <button>Wordpress</button>
          <button>Vue</button>
          <button>Bootstrap</button>
          <button>Laravel</button>
          <div class="subTitle-tools">
            <img src="/img/icono-tool.png" alt="">
            <h3 class="title-skills">{{ tec }}</h3>
          </div>
          <button>GitHub</button>
          <button>Jira</button>
          <button>Figma</button>
        </div>
      </div>
    </div>
    <div id="pro">
      <Projects v-show="vali == false" />
      <ProjectsEs v-show="vali == true" />
    </div>
    
    <div id="contact">
      <FootComponent v-show="vali == false" />
      <FootComponentEs v-show="vali == true" />
    </div>
    
  </main>
</template>

<style scoped>
  main {
    color: black;
  }

  .perfil {
    border-radius: 50%;
    width: 400px;
  }

  .inicio {
    display: flex;
    align-items: center;
    justify-content: center;
    margin: 250px 0 150px 0;
  }

  .info-inicio {
    margin-left: 100px;
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  .info-inicio p {
    font-size: 16px;
    font-weight: 600;
  }

  .info-inicio h2 {
    font-size: 48px;
    font-weight: bold;
  }

  .info-inicio h3 {
    font-size: 28px;
    font-weight: 600;
    color: rgb(85, 85, 85);
    margin-bottom: 10px;
  }

  .btn-info {
    display: flex;
    margin-bottom: 10px;
  }

  .btn-info a {
    color: white;
    
  }

  .btn-info .cv {
    width: 140px;
    height: 50px;
    border-radius: 50px;
    background-color: white;
    border: 1px solid black;
    margin-right: 10px;
    cursor: pointer;
  }

  .btn-info .info {
    width: 140px;
    height: 50px;
    border-radius: 50px;
    background-color: rgb(53, 53, 53);
    border: 1px solid rgb(53, 53, 53);
    color: white;
    cursor: pointer;
  }

  .btn-info .cv a {
    
    color: rgb(53, 53, 53);
   
  }

  .info-inicio .iconos img {
    width: 50px;
  }

  .about {
    display: flex;
    flex-direction: column;
    align-items: center;
    max-width: 1200px ;
    margin: 0 auto;
    padding-top: 100px;
  }

  .title-about {
    font-size: 48px;
    font-weight: 600;
  }

  .about-info {
    display: flex;
    margin-top: 50px;
  }

  .skills button {
    padding: 5px 10px;
    background-color: #ddddd5;
    border: 0;
    border-radius: 5px;
    margin: 5px;
    font-family: "Poppins", sans-serif;
    font-weight: 300;
    font-style: normal;
    font-size: 16px;
    color: black;
  }

  .skills .subTitle-skills {
    display: flex;
  }

  .skills .subTitle-tools {
    display: flex;
    margin-top: 20px;
  }

  .skills h3 {
    margin-left: 5px;
    font-weight: 600;
  }

  .skills img {
    width: 30px;
  }

  .about-text {
    width: 80%;
    padding-right: 50px; 
  }

  @media screen and (max-width: 1024px) {
    .inicio {
      flex-direction: column;
    }

    .info-inicio {
      margin: 50px 0 0 0;
    }
  }

  @media screen and (max-width: 715px) {
    .info-inicio h2 {
      font-size: 35px;
    }
  
    .info-inicio h3 {
      font-size: 20px;
    }
    
    .perfil {
      width: 250px;
    }

    .about-info {
      flex-direction: column;
    }

    .about-text{
      padding: 0;
      margin-bottom: 50px;
      width: 100%;
    }

    .title-about {
      font-size: 35px;
    }
  }
</style>
