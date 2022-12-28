<template>
    <div class="content">
        <ul>
            <LootboxItem />
            <LootboxItem />
            <LootboxItem />
            <LootboxItem />
            <LootboxItem />
            <LootboxItem />


        </ul>


    </div>
</template>


<script setup lang="ts">
import LootboxItem from './LootboxItem.vue'

</script>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
    name: 'LootboxItemArea',
})
</script>


<style scoped>

ul {
    width: 75%;
    display: flex;
    flex-wrap: wrap;
    list-style-type: none;
    padding: 0;
    gap: 25px;
}

.content {
    padding-top: 0;
}

</style>