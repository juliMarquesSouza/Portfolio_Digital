<template>
    <div class="Componente">
        <h1 class="title">{{ title }}</h1>
        <p class="text">{{ mensage }}</p>
    </div>
</template>

<script>
export default {
    name: "ComponentFrutas",
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
</script>

<style scoped>
.title {
    color: hsl(168, 34%, 41%);
    display: flex;
    align-items: center;
    justify-content: center;
    color: hsl(199, 67%, 34%);

}

.text {
    font-family: "Barlow", sans-serif;
    font-weight: 600;
    color: hsl(168, 34%, 41%);
    display: flex;
    align-items: flex-end;
    text-align: center;
    flex-direction: column;
    width: 25rem;
    font-size: 20px;
    color: hsl(199, 67%, 34%);
}

.Componente {
    height: calc(100% - 5rem);
    display: flex;
    flex-direction: column;
    justify-content: flex-end;
    padding: 0rem;
    gap: 2rem;
    margin: auto;
}
</style>