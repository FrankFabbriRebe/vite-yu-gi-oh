<script>

import AppCard from './AppCard.vue';
//import store
import { store } from '../store'

export default {
    name: "AppMain",

    components: {
        AppCard
    },

    data() {
        return {
            store,
        }
    },

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
    height: 500px;
}

.main_container {
    width: 90%;
    background-color: white;
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
    padding: 10px;
    /*  dedbug */
    height: 400px;
}
</style>
