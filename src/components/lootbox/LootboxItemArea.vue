<template>
    <div class="content">
        <ul>
            <LootboxItem
            v-for=" lootboxItem in lootboxItems" :key="lootboxItem.id"
             :title="lootboxItem.title" 
             :itemDescription="lootboxItem.itemDescription" 
             :imgSrc="lootboxItem.imgSrc" 
             :imgAlt="lootboxItem.imgAlt" 
             :percentChance="lootboxItem.percentChance"/>
        </ul>
            <Arrows />
            <AppButton text="Test my box"/>
            <AppButton text="Save my Box" />

    </div>
</template>


<script setup lang="ts">
// --------------------------------------------------------------
// Imports
// ---------------------------------------------------------------

// Components
import LootboxItem from './LootboxItem.vue'
import Arrows from '../blocks/Arrows.vue'
import AppButton from '../blocks/AppButton.vue'

// --------------------------------------------------------------
// Data, methods and functions
// ---------------------------------------------------------------

const props = defineProps([
        'lootboxItems'
    ])

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
    position: relative;
}

</style>