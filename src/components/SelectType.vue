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
</script>

<template>
    <!-- Dropdown Button -->
    <div class="dropdown pt-4">
        <select class="form-select" aria-label="Default select example" v-model="store.archetypeSelected"
            @change="$emit('filter')">
            <option value="" disabled selected>Choose Archetype</option>
            <option v-for="archetype in store.archetypeArray" :value="archetype.archetype_name">
                {{ archetype.archetype_name }}
            </option>
        </select>
    </div>
</template>

<style lang="scss" scoped></style>