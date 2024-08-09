<script setup lang="ts">
import LinkButton from "./LinkButton.vue";

defineProps({
    collection: Object
})

</script>

<template>
    <div class="collection-name">{{collection?.["collectionName"]}}</div>
    <div class="grid-container">
        <LinkButton v-for="item in collection?.['contents']" :link="item?.['link']" :text="item?.['text']"
            :owner="item?.['owner']"></LinkButton>
    </div>
</template>

<style scoped>

.collection-name {
    font-size: 20px;
    font-weight: bold;
    margin: 20px 0;
}

.grid-container {
    display: grid;
    column-gap: 2vw;
    row-gap:1vh;
    justify-content: center;
    margin: 0 auto;
    padding: 2vw;
}

@media (min-width: 1080px) {
    .grid-container {
        grid-template-columns: repeat(5, 1fr);
    }
}

@media (min-width: 768px) and (max-width: 1079px) {
    .grid-container {
        grid-template-columns: repeat(4, 1fr);
    }
}
@media (min-width: 576px) and (max-width: 767px) {
    .grid-container {
        grid-template-columns: repeat(3, 1fr);
    }
}

@media (min-width: 480px) and (max-width: 575px) {
    .grid-container {
        grid-template-columns: repeat(2, 1fr);
    }
}

@media (max-width: 479px) {
    .grid-container {
        grid-template-columns: 1fr;
    }
}
</style>