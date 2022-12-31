<template>

    <li class="lootbox-item">
        <i class="fa fa-window-close" aria-hidden="true"></i>
        <h3>{{ title }}</h3>
        <img :src="imgSrc" :alt="imgAlt">
        <span>{{ percentChance }}%</span>
    </li>

</template>


<script setup lang="ts">

const props = defineProps([
    'title', 'itemDescription', 'imgSrc', 'imgAlt', 'percentChance'
])

</script>



<style scoped>

.lootbox-item {
    text-align: center;
    border-radius: var(--border-containers);
    border: var(--light-grey) 1px solid;
    flex: 1 1 25%;
    max-width: 30%;
}

.lootbox-item img {
    width: 100%;
    height: 75px;
}

.lootbox-item span {
    display: block;
    padding: 0;
    margin: 0;
}

.fa-window-close {
    color: red;
    position: absolute;
    right: 10px;
    top: 2.5px;
    font-size: 25px;
    z-index: 10000;
    cursor: pointer;
}

@media screen and (min-width: 992px) {
    .lootbox-item {
        flex: 1 1 20%;
        max-width: 20%;
    }

    .lootbox-item img {
        width: 100%;
        height: 100px;
}
}

</style>