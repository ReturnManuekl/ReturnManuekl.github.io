<template>
    <div class="card-project">
        <img :src="img" alt="">
        <div>
            <h2>{{ title }}</h2> 
            <p>{{ text }}</p>
            <a :href=live target="_blank"><button>Live Demo</button></a>
        </div>
    </div>
</template>

<script setup>
    const props = defineProps([
        'value',
    ])
    const {
        title,
        img,
        text,
        repo,
        live,
    } = props.value
</script>

<style scoped>

    .card-project {
        display: flex;
        justify-content: center;
        margin-bottom: 50px;
    }

    .card-project img {
        width: 400px;
        height: 300px;
        object-fit: cover;
        margin-right: 50px;
        border-radius: 10px;
        opacity: .7;
    }
    .card-project img:hover {
        opacity: 1;
    }

    .card-project > div {
        width: 40%;
    }

    .card-project button:hover {
        cursor: pointer;
        background-color: white;
        color: black;
    }

    .card-project h2 {
        margin-bottom: 10px;
    }

    .card-project button {
        padding: 10px 20px;
        border: 1px solid rgb(53, 53, 53);
        border-radius: 50px;
        background-color: rgb(53, 53, 53);
        color: white;
        margin-top: 30px;
    }

    @media screen and (max-width: 1024px) {
    .card-project img {
        width: 300px;
        height: 225px;
        }
    }

    @media screen and (max-width: 715px) {
        .card-project {
            flex-direction: column;
            align-items: center;
        }
        
        .card-project > div {
            width: 100%;
        }
        
        .card-project img {
            width: 100%;
            margin-right: 0;
        }
    }

</style>