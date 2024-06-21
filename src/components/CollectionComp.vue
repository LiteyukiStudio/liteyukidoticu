<script setup lang="ts">
import LinkButton from "./LinkButton.vue";

defineProps({
    collection: Object
})

</script>

<template>
    <div class="collection-name">{{collection?.["collectionName"]}}</div>
    <LinkButton v-for="item in collection?.['contents']" :link="item?.['link']" :text="item?.['text']" :owner="item?.['owner']"></LinkButton>
</template>

<style scoped>
.collection-name {
    font-size: 20px;
    font-weight: bold;
    margin: 20px;
}
</style>