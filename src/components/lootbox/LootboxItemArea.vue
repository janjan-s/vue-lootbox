<template>
    <div class="content">
        <ul>
            <!-- <LootboxItem v-for"lootboxItems" /> -->
        </ul>
            <Arrows />
            <AppButton />
            <AppButton />

    </div>
</template>


<script setup lang="ts">
import LootboxItem from './LootboxItem.vue'
import Arrows from '../blocks/Arrows.vue'
import AppButton from '../blocks/AppButton.vue'

const props = defineProps([
        'lootboxItems'
    ])

</script>

<!-- <script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
    name: 'LootboxItemArea',
})
</script> -->


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