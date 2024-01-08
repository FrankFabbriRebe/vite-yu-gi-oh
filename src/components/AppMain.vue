<script>

import AppCard from './AppCard.vue'

export default {
    name: "AppMain",

    components: {
        AppCard
    }
}

</script>

<template>
    <main>
        <div class="main_container">
            <AppCard />
        </div>
    </main>
</template>

<style lang="scss" scoped>
main {
    background-color: bisque;
    display: flex;
    justify-content: center;
    align-items: center;
    /* debug */
    // height: 500px;
}

.main_container {
    width: 90%;
    margin-top: 50px;
    background-color: white;
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
    justify-content: center;
    padding: 10px;
    /*  dedbug */
    // height: 200px;
}
</style>
