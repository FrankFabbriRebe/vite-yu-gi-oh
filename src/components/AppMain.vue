<script>

// import components
import AppCard from './AppCard.vue';
import SelectType from './SelectType.vue';

//import store
import { store } from '../store'

export default {
    name: "AppMain",

    components: {
        AppCard,
        SelectType
    },

    data() {
        return {
            store,
        }
    },

}
// console.log(store.cardList);

</script>

<template>
    <main>
        <SelectType />
        <div class="main_container">
            <AppCard v-for="card in store.cardList" :info="card" />
        </div>
    </main>
</template>

<style lang="scss" scoped>
main {
    background-color: bisque;
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 10px;
    flex-direction: column;
    /* debug */
    // height: 500px;
}

.main_container {
    width: 90%;
    background-color: white;
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
    padding: 10px;
    /*  dedbug */
    // height: 400px;
}
</style>
