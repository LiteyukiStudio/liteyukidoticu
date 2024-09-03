<script setup lang="ts">
import CollectionComp from "./components/CollectionComp.vue";
import {onMounted, ref} from "vue";
import {statsApi, uploadVisitRecord} from "./components/scripts/statsApi.ts";

let collections = ref([])
let totalVisit = ref(0)
let currentVisit = ref(0)

fetch("data_source.json")
    .then(response => response.json())
    .then(data => {
        collections.value = data
        console.log(data)
    })

onMounted(async () => {
    await uploadVisitRecord();
    totalVisit.value = await statsApi.getVisitCount();
    currentVisit.value = await statsApi.getCurrentVisitCount();
});


</script>

<template>
    <div class="title">Liteyuki Index 索引站</div>
    <CollectionComp v-for="c in collections" :collection="c"></CollectionComp>
    <footer>
        <p>Liteyuki Studio | 总计到访者: {{ totalVisit }} | 你是第 {{ currentVisit }} 位</p>
    </footer>
</template>

<style scoped>

body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f0f0f0;
}

.title {
    font-size: 24px;
    font-weight: bold;
    margin: 20px;
}
</style>
