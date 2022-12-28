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

/* li.lootbox-item {
    flex: 1 1 21%;
    border-radius: var(--border-containers);
    border: var(--light-grey) 1px solid;
    text-align: center;
    max-width: 21%;
    display: flex;
    flex-direction: column;
}

li h3 {
    flex: 1 1 25%;
}

li span {
    flex: 1 1 25%;
}

li img {
    margin-bottom: 0;
    padding: 0;
    flex: 1 1 50%;
}

span {
    display: block;
    border-top: var(--light-grey) 1px solid;
} */

</style>