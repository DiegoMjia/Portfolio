<script setup lang="ts">
defineOptions({
    name: 'FooterPage'
})
</script>

<template>
    <div class="footerPage">
        <p>♥/2025</p>
    </div>
</template>


<style scoped>
.footerPage {
    width: 100%;
    opacity: 0.5;
    margin-top: 100px;
    background-color: #1b1e23;
}
</style>

<style>
body.active {
    .footerPage {
        opacity: 1;
        background-color: transparent;
        color: #323232;
    }
}
</style>