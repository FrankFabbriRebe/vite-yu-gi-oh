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

}

// console.log(store.archetype);

</script>

<template>
    <div class="dropdown">
        <button class="btn btn-secondary dropdown-toggle" type="button" data-bs-toggle="dropdown" aria-expanded="false">
            Select archetype
        </button>
        <ul class="dropdown-menu">
            <li v-for="element in store.apiArchetype"><a class="dropdown-item" href="#">{{ element.archetype_name }}</a>
            </li>
        </ul>
    </div>
</template>

<style lang="scss" scoped></style>