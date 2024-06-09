<template>
    <div class="container">
        <div class="frameTitle">
            <h1 class="title">{{ title }}</h1>
        </div>
        <p class="text">{{ mensage }}</p>
        <div>
            <button class="button">Learn More</button>
            <span></span>
        </div>
    </div>
</template>

<script>
export default {
    name: "PropsButton",
    props: {
        title: {
            type: String,
            required: true,
        },
        mensage: {
            type: String,
            required: true,
        }
    }
}

name: "PropsButton";
</script>

<style scoped>
.frameTitle {
    width: 25rem;
}

.container {
    display: flex;
    flex-direction: column;
    padding: 5rem;
    gap: 2rem;
}

.title {

    color: #243141;
    font-size: 50px;
}

.text {
    font-family: "Barlow", sans-serif;
    font-weight: 400;
    font-style: normal;
    color: hsl(251, 7%, 71%);
    font-size: 20px;
}

.button {
    /* border-bottom: 8px solid orange; */
    color: #243141;
    width: 120px;
    background: transparent;
    border: none;
    font-family: "Fraunces", sans-serif;
    font-weight: 900;
    font-size: 20px;
    cursor: pointer;
    position: relative;
    display: grid;
    z-index: 99;

}

span {
    background-color: orange;
    height: 0.7rem;
    border-radius: 1rem;
    position: relative;
    bottom: 0.5rem;
    z-index: 7;
    display: flex;
    width: 120px;
}
</style>