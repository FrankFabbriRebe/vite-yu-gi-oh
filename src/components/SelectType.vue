<script>

//import store
import { store } from '../store'

export default {
    name: "SelectType",

    data() {
        return {
            store,
        }
    },

    methods: {
        search(element) {
            this.store.archetypeSelected = element.archetype_name,
                console.log(this.store.archetypeSelected);
        }
    }

}
</script>

<template>
    <div class="dropdown">
        <button class="btn btn-secondary dropdown-toggle" type="button" data-bs-toggle="dropdown" aria-expanded="false">
            Select archetype
        </button>
        <ul class="dropdown-menu">
            <li v-for="element in store.apiArchetype" @click="search(element)"><a class="dropdown-item" href="#">{{
                element.archetype_name }}</a>
            </li>
        </ul>
    </div>
</template>

<style lang="scss" scoped></style>