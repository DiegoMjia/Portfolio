<script setup lang="ts">
defineOptions({
    name: 'BodyPortfolio',
})
</script>

<template>
    <div class="mainContainer">
        <div class="titleContainer">
            <h1>¡Hola, mi nombre es <b style="color: #646cff; font-weight: bold;">Diego!</b></h1>
            <section class="textContainer">
                <p style="line-height: 1.6;">
                    Desarrollador <b>web full-stack</b>. Gestiono proyectos de alto nivel, creando sitios web
                    con un alto estándar de <b>calidad</b>.
                </p>
            </section>
        </div>
    </div>
</template>

<style scoped>
.mainContainer {
    width: 50vw;
    height: 100%;
    display: flex;
    flex-direction: column;
    align-items: start;
}

h1, p {
    color: #fff;
    text-align: left;
}

.textContainer{
    display: flex;
    justify-content: center;
}

.titleContainer {
    min-width: 500px;
    display: flex;
    margin-left: 110px;
    flex-direction: column;
    align-items: center;
    margin-top: 150px;
}

h1 {
    font-size: 80px;
    font-weight: bold;
    margin: 20px auto;
}

@media (max-width: 768px) {
    .mainContainer {
        width: 100%;
        padding: 5px;
        justify-content: center;

    }

    .titleContainer {
        min-width: 0;
        margin-top: 10px;
        width: 100%;
        margin-left: 0;
    }

    p {
        text-align: center;
    }
    
    h1 {
        font-size: 40px;
        margin: 10px;
        margin-top: 10%;
        text-align: center;
    }

    .ContainerArrow {
        display: none;
    }
    
}
</style>

<style>
body.active {
    h1 {
        color: #000;
    }

    p {
        color: #000;
    }
}
</style>