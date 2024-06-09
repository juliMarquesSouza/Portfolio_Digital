<template>
    <div class="navbar">
        <h5> sunnyside </h5>
        <div class="menu">
            <ButtonServices @click.native="teste" class="btn-desktop" v-for="(button, index) in enderecos" :key="index"
                :title="button.title" :link="button.link" />

            <button class="btn-menuMobile" @click="showMenu"></button>
            <MenuMobile v-if="status" />
        </div>
    </div>
    <div class="banner">
        WE ARE CREATIVES
        <img class="img" src="../../assets/img/image-header_2.jpg" alt="header">
    </div>
</template>

<script setup>
import ButtonServices from '../atomos/ButtonServices.vue';
import MenuMobile from "../atomos/MenuMobile.vue";
import { ref } from "vue";

const status = ref(false)

function showMenu() {
    // .value is needed in JavaScript
    status.value = !status.value
}
const menuMobile = (false);
let enderecos = [
    { title: "About", link: "" },
    { title: "Services", link: "" },
    { title: "Projects", link: "" },
    { title: "Contact", link: "" },
]

</script>

<style scoped>
.banner {
    font-size: 40px;
    color: hsl(0, 0%, 100%);
    display: flex;
    justify-content: flex-end;
    flex-direction: column;
    align-items: center;
    height: calc(100% - 4rem - 40px);
    background: hsl(199.9deg 100% 62.16%);

}

.navbar {
    height: 4rem;
    text-align: center;
    align-items: center;
    display: flex;
    gap: 40px;
    padding: 20px 30px;
    justify-content: space-between;
}

.btn-menuMobile {
    display: none;
}

h5 {

    font-weight: 900;
    font-size: 20px;
    color: hsl(0, 0%, 100%);
}

.img {
    width: 40%;

}

@media screen and (max-width: 768px) {
    .btn-menuMobile {
        background: transparent;
        width: 2rem;
        height: 2rem;
        background-image: url("../../assets/icons/icons8-menu.svg");
        background-repeat: no-repeat;
        background-size: cover;
        border: none;
        display: block;
    }

    .btn-desktop {
        display: none;
    }
}
</style>
