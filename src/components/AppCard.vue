<script>

export default {
    name: "AppCard"
}

</script>

<template>
    <div class="card">
        <h1>Img</h1>
        <h2>Name</h2>
        <h3>Type</h3>
    </div>
</template>

<style lang="scss" scoped>
.card {
    background-color: bisque;
    width: calc(100% / 5 - 10px);
    display: flex;
    flex-direction: column;
    align-items: center;
    // debug
    height: 100px;
}
</style>