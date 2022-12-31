<template>
    
    <div class="lootbox-container">
        <LootboxHeader />
        <LootboxItemArea :lootboxItems="lootboxItems" />
    </div>

</template>


<script setup lang="ts">
// --------------------------------------------------------------
// Imports
// ---------------------------------------------------------------

// Components
import LootboxHeader from './LootboxHeader.vue';
import LootboxItemArea from './LootboxItemArea.vue'

// Modules
import { defineProps } from 'vue';

// Types
import type LootboxItem from '../types/LootboxItem';

// --------------------------------------------------------------
// Data, methods and functions
// ---------------------------------------------------------------

const props = defineProps([
    'lootboxItems'
])

</script>


<style scoped>
.lootbox-container {
  background: #fff;
  filter: var(--drop-shadow);
  margin: var(--mobile-gutters);
  border-radius: var(--border-containers);
}

@media screen and (min-width: 1200px) {
    .lootbox-container {
        width: 70%;
        margin-bottom: 0;
        margin-top: 20px;
    }
}

</style>