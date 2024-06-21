<script setup lang="ts">
import CollectionComp from "./components/CollectionComp.vue";
import {ref} from "vue";

let collections = ref([])

fetch("data_source.json")
    .then(response => response.json())
    .then(data => {
        collections.value = data
        console.log(data)
    })

</script>

<template>
    <div class="title">Liteyuki Index</div>
    <CollectionComp v-for="c in collections" :collection="c"></CollectionComp>
</template>

<style scoped>


.title {
    font-size: 24px;
    font-weight: bold;
    margin: 20px;
}
</style>
