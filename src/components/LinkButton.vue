<script setup lang="ts">


const props = defineProps({
    text: String,
    link: String,
    owner: String,
})

let imgSrc = ""

if(props.owner){
    imgSrc = `https://github.com/${props.owner}.png?size=80`
}

</script>

<template>
    <a class="button" :href="link">
        <img v-if="imgSrc!=''" :src="imgSrc" style="width: 40px; height: 40px; border-radius: 50%; margin-right: 10px; margin-left: 10px;" alt=""/>
        {{text}}
    </a>
</template>

<style scoped>
a.button {
    align-content: center;
    display: flex;
    align-items: center;
    justify-content: center;
    margin: 10px auto;
    padding: 15px 15px;
    color: #fff;
    text-decoration: none;
    background-color: #a2d8f4;
    border-radius: 80px;
    transition: background-color .3s ease;
    max-width: 100%
}

a.button:hover {
    background-color: #d0e9ff
}

@media (max-width: 1080px) {
    a.button {
        width:calc(100% - 20px)
    }
}

</style>