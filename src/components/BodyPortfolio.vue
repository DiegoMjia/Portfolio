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
                <p style="max-width: 540px; line-height: 1.6;">
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

.textContainer{
    display: flex;
    justify-content: center;
}

.titleContainer {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    margin-top: 150px;
}

p {
    text-align: left
}

h1 {
    font-size: 80px;
    font-weight: bold;
    text-align: start;
    margin: 20px;
    margin-left: 110px;
}

@media (max-width: 768px) {
    .mainContainer {
        width: 100%;
        padding: 5px;
    }

    .titleContainer {
        margin-top: 0;
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
