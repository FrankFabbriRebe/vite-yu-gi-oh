<script>

export default {
    name: "AppCard",

    props: {
        info: Object,
    },

}
</script>

<template>
    <div class="card">
        <img :src="info.card_images[0].image_url" :alt="info.name">
        <h2>{{ info.name }}</h2>
        <span>{{ info.archetype }}</span>
    </div>
</template>

<style lang="scss" scoped>
.card {
    background-color: bisque;
    width: calc(100% / 5 - 10px);
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
    // debug
    // height: 100px;
}

h2 {
    color: white;
    margin-bottom: 5px;
}

img {
    width: 100%;
}
</style>