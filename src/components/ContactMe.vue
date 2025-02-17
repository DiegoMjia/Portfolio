<script setup lang="ts">
defineOptions({
    name: 'ContactMe'
})
</script>

<template>
    <div class="contactMe">
        <h2 style="font-size: 60px; text-align: start;" id="Contacto">Contacto</h2>
        <div class="Container">
            <section class="Linkedin">
                <div class="box">
                    <a href="https://www.linkedin.com/in/diego-mejia-webdev/" target="_blank"
                        style="height: 100%; width: 100%; display: inline-block;">
                        <div class="Circle">
                            <div class="logoLinkedin">

                            </div>
                        </div>
                        <p>Diego Mejia</p>
                        <span class="send">
                        </span>
                    </a>
                </div>
            </section>

            <section class="Github">
                <div class="box">
                    <a href="https://github.com/DiegoMjia" target="_blank"
                        style="height: 100%; width: 100%; display: inline-block;">
                        <div class="Circle">
                            <div class="logoGithub">

                            </div>
                        </div>
                        <p>DiegoMjia</p>
                        <span class="send">
                        </span>
                    </a>
                </div>
            </section>

            <section class="Email">
                <div class="box">
                    <a href="mailto:mjiadiego@gmail.com" style="height: 100%; width: 100%; display: inline-block;">
                        <div class="Circle">
                            <div class="logoEmail">

                            </div>
                        </div>
                        <p>mjiadiego@gmail.com</p>
                        <span class="send">
                        </span>
                    </a>
                </div>
            </section>
        </div>
    </div>
</template>

<style scoped>
.contactMe {
    margin-left: 110px;
    height: 100%;
    display: flex;
    margin-top: 180px;
    flex-direction: column;
}

.send {
    position: absolute;
    bottom: 0;
    right: 0;
    margin: 15px;
    background-image: url('../img/Images/send-dark-theme-v2.svg');
    background-size: cover;
    height: 30px;
    width: 30px;
    transition: all 0.3s ease-in-out;
}

a {
    padding: 15px;

}

.Container {
    display: flex;
    flex-direction: row;
    gap: 25px;
}

.Circle {
    border-radius: 50%;
    outline: 1px solid #ffffff;
    width: fit-content;
    height: fit-content;
    padding: 10px;
}

.box {
    cursor: pointer;
    min-width: 300px;
    height: 160px;
    border-radius: 20px;
    outline: 3px solid #ffffff;
    position: relative;
    transition: all 0.3s ease-out;

}

.box:hover {
    transform: scale(1.1);

    .send {
        background-image: url('../img/Images/send-dark-theme-v2-changed.svg');
    }
}

.logoLinkedin {
    height: 15px;
    width: 15px;
    background-size: contain;
    padding: 15px;
    background-image: url('../img/LinkedinIcons/linkedin-dark-theme.svg');
}

.logoGithub {
    height: 15px;
    width: 15px;
    background-size: contain;
    padding: 15px;
    background-image: url('../img/GithubIcons/Github-dark-theme.svg');
}

.logoEmail {
    height: 15px;
    width: 15px;
    background-size: contain;
    padding: 15px;
    background-image: url('../img/GmailIcons/gmailNoMoreThemes.svg');
}

a p {
    position: absolute;
    bottom: 0;
    padding: 20px;
}

@media (max-width: 768px) {
    .contactMe {
        margin-left: 0;
        margin-top: 0;
        flex-direction: column;
        align-items: center;
    }

    .Container {

        flex-direction: column;
        align-items: center;
    }
}
</style>


<style>
body.active {
    .box {
        outline: 3px solid #0a0a0a;
    }

    .Circle {
        outline: 1px solid #0a0a0a;
    }

    a {
        color: #0a0a0a;
    }

    a:hover {
        color: #535bf2;
    }

    .logoLinkedin {
        background-image: url('../img/LinkedinIcons/linkedin-light-theme.svg');
    }

    .logoGithub {
        background-image: url('../img/GithubIcons/Github-light-theme.svg');
    }

    .send {
        background-image: url('../img/Images/send-light-theme-v2.svg');
    }

    .box:hover {
        .send {
            background-image: url('../img/Images/send-light-theme-v2-changed.svg');
        }
    }

}
</style>