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

a {
    max-width: 300px;
}

a.button {
    box-sizing: border-box;
    align-content: center;
    display: flex;
    align-items: center;
    justify-content: center;
    margin: 10px auto;
    padding: 15px 15px;
    color: #fff;
    text-decoration: none;
    position: relative;
    background-color: #a2d8f4;
    border-radius: 5px;
    transition: background-color .3s ease;
    width: 100%;
    z-index: 1;
}

a.button::after {
    content: "";
    position: absolute;
    bottom: 0;
    left: 0;
    width: 100%;
    height: 100%;
    border-radius: 5px;
    background-color: #d0e9ff;
    transform: scaleY(0);
    transform-origin: bottom;
    transition: transform 0.3s ease;
    z-index: -1;
}
a.button:hover::after {
    transform: scaleY(1);
    
}

</style>