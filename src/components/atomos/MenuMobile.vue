<template>
    <div class="topnav">
        <a v-for="(item, index) in enderecos" :key="index" :href="item.link" target="_blank" class="btn-about">{{
            item.title }}</a>
    </div>
</template>

<script setup>
let enderecos = [
    { title: "About", link: "" },
    { title: "Services", link: "" },
    { title: "Projects", link: "" },
    { title: "Contact", link: "" },
]

</script>

<style scoped>
.topnav {
    display: none;
}

@media screen and (max-width: 768px) {
    .btn-about {
        font-family: "Barlow", sans-serif;
        font-weight: 800;
        font-size: 15px;
        margin: auto;
        font-weight: 300;
        font-size: 20px;
        color: hsl(250, 5%, 58%);
        padding: 15px;
        text-decoration: none;
        border-radius: 1.5rem;
        cursor: pointer;
        width: 7rem;
    }

    .btn-about:hover {
        font-family: "Fraunces", sans-serif;
        font-weight: 900;
        font-size: 16px;
        background-color: hsl(51, 100%, 50%);
        border-radius: 1.5rem;
        transition: 0.3s;
        color: black;
    }

    .topnav {
        width: 90%;
        height: 15rem;
        background: white;
        position: fixed;
        top: 0;
        right: 3rem;
        padding: 20px;
        margin-top: 6rem;
        display: grid;
        color: hsl(250, 5%, 58%);
    }
}
</style>
