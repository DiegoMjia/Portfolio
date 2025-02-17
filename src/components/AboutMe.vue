<script setup lang="ts">
defineOptions({
    name: 'AboutMe'
})
</script>

<template>
    <div>
        <section class="AboutMe" style=" margin-top: 20%; margin-bottom: 20%;" id="SobreMi">
            <div class="PresentationOfMyself">
                <h2 style="font-size: 40px; font-weight: bold;">Sobre mí</h2>
                <p style="line-height: 1.6;">Me apasiona el mundo del <b style="color: #535bf2;">desarrollo web</b>. Disfruto creando páginas
                    con
                    atención al detalle,
                    cuidando cada aspecto <b>para ofrecer la mejor experiencia
                        posible</b> <b style="color: #01d890;">(UI/UX)</b>. Siempre me ha fascinado el
                    potencial de los navegadores y cómo pueden llevar la <b
                        style="color: #fb0102; font-weight: bold;">experiencia del usuario a otro nivel.</b></p>
                <br>
                <p style="line-height: 1.6;">
                    Me encanta el frontend, pero también tengo experiencia en backend con <b
                        style="color: #01d890;">Node.js</b> y <b style="color: #535bf2;">Express.js</b>. Y amo <b>JavaScript</b>, con sus peculiaridades <b
                        style="color: #f7e025;">♥</b>.
                </p>
            </div>
            <div class="Animation">
                <div class="Container">
                    <img src="../img/Gifs and animations/Loading Square.gif" alt="HTML5">
                </div>
            </div>
        </section>
    </div>
</template>


<style scoped>
.AboutMe {
    scroll-margin-top: 20rem;
    width: 100%;
    display: flex;
    flex-direction: column;
}

.PresentationOfMyself {
    position: relative;
    margin-left: 110px;
    display: inline-block;
    text-align: left;
    max-width: 600px;
}

b {
    font-weight: bold;
    overflow-wrap: break-word;
    opacity: 1;
    color: #ffffff;
}

.Container {
    border-radius: 100%;
    z-index: 100;
    width: 281px;
    height: 281px;
    outline: 5px solid rgb(255, 255, 255);
}

.Container img {
    border-radius: 100%;
    width: 100%;
    height: 100%;
}

.Animation {
    object-fit: cover;
    position: absolute;
    right: 0;
    margin-right: 200px;
}

body.active {
    b {
        color: #000;
    }

    .Container {
        outline: 5px solid rgb(0, 0, 0);
        background-color: #000;
    }
}

@media (max-width: 768px) {
    .PresentationOfMyself {
        margin: 20px;
    }

    .Animation {
        display: none;
    }
}
</style>