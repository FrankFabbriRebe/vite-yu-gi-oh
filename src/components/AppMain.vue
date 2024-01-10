<script>

// import components
import AppCard from './AppCard.vue';
import SelectType from './SelectType.vue';

//import store
import { store } from '../store';

// import axios
import axios from 'axios';

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

    methods: {

        // call general api
        getCard() {

            let filteredUrl = store.apiURL;

            if (store.archetypeSelected) {
                filteredUrl += `&archetype=${store.searchArchetype}`
            }

            axios
                .get(filteredUrl)
                .then((res => {
                    // console.log(res.data);
                    store.cardList = res.data.data
                }))
                .catch((err) => {
                    console.log("Errors", err);
                })
        },

        // call api for archetype
        getArchetype() {
            axios
                .get(store.apiArchetype)
                .then((res => {
                    // console.log(res.data);
                    store.archetypeArray = res.data
                }))
                .catch((err) => {
                    console.log("Errors", err);
                })
        }

    },

    created() {
        this.getCard();
        this.getArchetype()
    }

}


</script>

<template>
    <main>
        <SelectType @filter="getCard" />
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
