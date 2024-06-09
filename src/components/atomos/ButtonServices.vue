<template>
    <a :href="link" target="_blank" class="btn-about">{{ title }}</a>
</template>

<script>
export default {
    name: "button",
    props: {
        title: {
            type: String,
            required: true,
        },
        link: {
            type: String,
            required: true,
        }
    }
}
</script>

<style>
.btn-about {
    font-weight: 300;
    font-size: 16px;
    color: hsl(0, 0%, 100%);
    padding: 15px;
    text-decoration: none;
    border-radius: 1.5rem;
    cursor: pointer;
}

.btn-about:hover {
    font-weight: 600;
    font-size: 16px;
    background-color: hsl(200, 100%, 72%);
    border-radius: 1.5rem;
    transition: 0.3s;
}
</style>
