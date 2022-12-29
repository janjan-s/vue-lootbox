<template>

    <li class="lootbox-item">
        <h3>Title</h3>
        <img src="https://via.placeholder.com/100" alt="">
        <span>50%</span>
    </li>

</template>


<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
    name: 'LootboxItem',
})
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