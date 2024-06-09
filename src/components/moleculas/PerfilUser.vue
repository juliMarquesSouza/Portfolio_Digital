<template>
    <div class="container">
        <section class="userClient">
            <img :src="imgSrc">
            <span class="feedbackClient">{{ mensage }}</span>
        </section>
        <section class="bioUsers">
            <h4>{{ nomeTitle }}</h4>
            <span class="infoUsers">{{ userTitle }}</span>
        </section>
    </div>

</template>

<script>
export default {
    name: "PerfilUser",
    props: {
        mensage: {
            type: String,
            required: true,
        },
        imgSrc: {
            type: String,
            required: true,
        },
        altImg: {
            type: String,
            required: true,
        },
        nomeTitle: {
            type: String,
            required: true,
        },
        userTitle: {
            type: String,
            required: true,
        },

    },
}


</script>

<style scoped>
.feedbackClient {
    font-family: "Barlow", sans-serif;
    font-weight: 800;
    color: hsl(240, 1%, 49%);
    text-align: center;
    font-size: 15px;
    line-height: 20px;
}

.container {
    display: flex;
    align-items: center;
    flex-direction: column;
    gap: 1rem;
    font-family: "Fraunces", sans-serif;
    font-weight: 900;
}

.userClient {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    width: 50%;
    padding: 5rem;
    gap: 3rem;
    font-family: "Fraunces", sans-serif;
    font-weight: 900;
}

.infoUsers {
    font-family: "Barlow", sans-serif;
    font-weight: 500;
    color: hsl(240, 1%, 49%);
}

.bioUsers {
    display: grid;
    place-items: center;
    gap: 10px;
}

img {
    border-radius: 50%;
    height: 80px;
}
</style>