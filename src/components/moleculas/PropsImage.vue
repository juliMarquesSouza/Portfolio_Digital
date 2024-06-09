<template>
    <img :src="imageSrc">
</template>

<script>
export default {
    name: "Section8",
    props: {
        imageSrc: {
            type: String,
            required: true,
        },
    }
}
</script>

<style scoped>
img {
    width: 25%;
    height: auto;
}
</style>