<script setup lang="ts">
defineOptions({
    name: 'Habilities'
})
</script>

<template>
    <div class="containerHabilities">
        <h2>Habilidades</h2>
        <p class="textTec">Tecnologías</p>
        <br>
        <div class="conteinerTecnologies">
            <div class="HTMLBox">
                <img src="../img/HabilitiesImages/html-logo.svg" alt="HTML logo">
                <p>HTML 5</p>
            </div>

            <div class="CSSBox">
                <img src="https://upload.wikimedia.org/wikipedia/commons/a/ab/Official_CSS_Logo.svg" alt="CSS logo">
                <p>CSS 3</p>
            </div>

            <div class="boxJs">
                <img src="https://upload.wikimedia.org/wikipedia/commons/9/99/Unofficial_JavaScript_logo_2.svg" alt="Js logo">
                <p>JavaScript</p>
            </div>

            <div class="TypeScriptBox">
                <img src="https://upload.wikimedia.org/wikipedia/commons/4/4c/Typescript_logo_2020.svg" alt="TypeScript logo">
                <p>TypeScript</p>
            </div>

            <div class="NodeJS">
                <img src="https://upload.wikimedia.org/wikipedia/commons/d/d9/Node.js_logo.svg" alt="Lit logo">
                <p>Node js</p>
            </div>

            <div class="ExpressBox">
                <img src="../img//icons8-express-js-80.png" alt="Express logo">
                <p>Express.js</p>
            </div>

            <div class="VueBox">
                <img src="https://upload.wikimedia.org/wikipedia/commons/9/95/Vue.js_Logo_2.svg" alt="Vue logo">
                <p>Vue.js</p>
            </div>

            <div class="MySQLBox">
                <img src="https://upload.wikimedia.org/wikipedia/commons/0/0a/MySQL_textlogo.svg" alt="MySQL logo">
                <p>MySQL</p>
            </div>

            <div class="GitBox">
                <img src="https://upload.wikimedia.org/wikipedia/commons/6/62/Git-logo-orange.svg" alt="Git logo">
                <p>Git</p>
            </div>
        </div>
    </div>
</template>


<style scoped>
.containerHabilities {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    margin: 25px;
    margin-right: 100px;
    position: absolute;
    right: 0;
    top: 175px;
    max-width: 500px;
}

.MySQLBox img {
    width: 70px;
    height: 40;
    object-fit: contain;
}

.VueBox img {
    width: 70px;
    height: 40;
    
    object-fit: contain;
}

.ExpressBox img {
    width: 70px;
    height: 40;

    object-fit: contain;
}

.conteinerTecnologies {
    display: flex;
    flex-direction: row;
    gap: 35px;
    flex-wrap: wrap;
}

.conteinerTecnologies > * {
    flex: 1 1 calc((100% - 70px) / 3);
    box-sizing: border-box;
}

.NodeJS img {
    width: 70px;
    height: 40;

    object-fit: contain;
}

.GitBox img {
    width: 70px;
    height: 40;

    object-fit: contain;
}

img {
    width: 50px;
    height: 50px;
    object-fit: contain;
}

@media (max-width: 768px) {
    .containerHabilities {
        position: relative;
        margin: 0;
        top: 20px;
        left: 0;
        max-width: 100%;
        width: 100%;
    }

    .conteinerTecnologies {
        gap: 10px;
    }

    .conteinerTecnologies {
        flex-direction: row;
    }
}
</style>