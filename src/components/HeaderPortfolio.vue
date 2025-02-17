<script setup lang="ts">
import { ref, onMounted } from 'vue'

defineOptions({
    name: 'HeaderPortfolio'
})

const containerTogle = ref<HTMLElement | null>(null)
const body = ref<HTMLElement>(document.body)
const HeaderContainer = ref<HTMLElement | null>(null)

const Menu = ref<HTMLElement | null>(null)
const overlay = ref<HTMLElement | null>(null)
const ShowMenu = () => {
    Menu.value?.classList.toggle('active')
    overlay.value?.classList.toggle('active')

}

onMounted(() => {
    containerTogle.value?.addEventListener('click', () => {
        body.value?.classList.toggle('active'),
            containerTogle.value?.classList.toggle('active')
        HeaderContainer.value?.classList.toggle('active')
    })
})

</script>

<template>
    <div class="HeaderPortfolio">
        <div class="HeaderContainer" ref="HeaderContainer">
            <div class="overlay" ref="overlay" @click="ShowMenu"></div>
            <h2 style="font-size: 30px;">MJia</h2>
            <span class="separator">|</span>
            <p
                style="font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif; font-size: 15px;">
                Portfolio</p>
            <span class="Menu" @click="ShowMenu">

            </span>
            <div class="ContainerMenu" ref="Menu">
                <ul class="ulMobileDesign">
                    <li><a href="#SobreMi">Sobre mí</a></li>
                    <!-- <li><a href="">Proyectos</a></li> -->
                    <li><a href="#Contacto">Contacto</a></li>
                </ul>
            </div>

            <ul class="ListDesktop">
                <li><a href="#SobreMi">Sobre mí</a></li>
                <!-- <li><a href="">Proyectos</a></li> -->
                <li><a href="#Contacto">Contacto</a></li>
                <span class="separatorV2" style="font-weight: bolder; margin-right: 19px;">|</span>
                <div id="containerTogle" ref="containerTogle">
                    <div class="Toggle"></div>
                </div>
            </ul>
        </div>
    </div>
</template>

<style scoped>
.HeaderPortfolio {
    position: sticky;
    top: 0;
    z-index: 100;
    width: 100%;
}

.HeaderContainer {
    backdrop-filter: blur(10px);
    display: flex;
    flex-direction: row;
    width: 100%;
    height: 88px;
    background-color: transparent;
    align-items: center;
    border-bottom: 1px solid #ffffff;
    transition: background-color 0.5s ease;
}

h2 {
    padding-left: 85px;
}

/* 
h2:hover {
    //Efecto glitch
} */

li {
    align-content: center;
    width: 150px;
    padding: 15px;
    user-select: none;
    margin: 0;
}

li {
    font-size: 15px;
    transition: font-size 0.5s ease-in-out;
    font-weight: bold;
}

li:hover {
    font-size: 16px;
    color: #535bf2;
}

.separator {
    color: #666;
    font-weight: 300;
    margin: 10px;
}

.ListDesktop {
    position: absolute;
    right: 50px;
    display: flex;
    flex-direction: row;
    list-style: none;
    align-items: center;
    cursor: pointer;
    height: 100%;
}

.HeaderLine {
    position: relative;
    top: 0;
    width: 100%;
    height: 10%;
    outline: 1px solid #ccc;
}

#containerTogle {
    background-color: #15171c;
    position: relative;
    width: 70px;
    height: 30px;
    box-shadow: inset 4px 4px 6px #4b4b4b;
    cursor: pointer;
    border-radius: 25px;
    margin: 0px auto;
    background-color: rgba(24, 49, 83, 1);
    transition: all 0.5s ease-in-out;
}

.Toggle {
    position: absolute;
    top: 0;
    left: 0;
    width: 30px;
    height: 30px;
    background-color: #ffffff;
    border-radius: 50%;
    transform: scale(.7);
    transition: all .3s ease-in-out;
    box-shadow: 3px 3px 8px #c4c4c4,
        -3px -3px -8px #ffffff;
}

#containerTogle.active .Toggle {
    left: 40px;
    background-color: #ffd43b;
}

#containerTogle.active {
    background-color: #ccc;
}

.HeaderContainer.active {
    background-color: transparent;
    backdrop-filter: blur(10px);
    color: #000000;
    border-bottom: 1px solid #000000;

    a {
        color: #000;
    }
}

.Menu {
    cursor: pointer;
    display: none;
    background-image: url('../img/Images/menu-hamburguesa-dark-theme.svg');
    background-size: cover;
    height: 40px;
    width: 30px;
    position: absolute;
    top: 0;
    margin: 20px;
    right: 0;
    z-index: 20;
}

.ContainerMenu {
    padding-top: 100px;
    background-color: #202020;
    position: absolute;
    right: 0;
    top: 0;
    width: 40%;
    height: 100vh;
    display: none;
}

.overlay {
    position: fixed;
    top: 0;
    left: 0;
    width: 100vw;
    height: 100vh;
    background: rgba(0, 0, 0, 0.7);
    backdrop-filter: blur(5px);
    z-index: 5;
    display: none;
}

.overlay.active {
    display: block;
}

.ContainerMenu.active {
    display: flex;
    z-index: 10;

    ul {
        flex-direction: column;
        list-style: none;
    }
}

@media (max-width: 768px) {
    .HeaderPortfolio .ListDesktop {
        display: none;
    }

    .Menu {
        display: flex;
    }

    h2 {
        padding-left: 10px;
    }
}
</style>


<style>
body.active {
    background-color: #f0f0f0;
    color: #000000;

}
</style>