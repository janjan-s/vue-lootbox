<template>
    
    <div class="lootbox-container">
        <LootboxHeader />
        <LootboxItemArea />
    </div>

</template>


<script setup lang="ts">
    import LootboxHeader from './LootboxHeader.vue';
    import LootboxItemArea from './LootboxItemArea.vue'
</script>


<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
    name: 'LootboxArea',
})
</script>

<style scoped>
.lootbox-container {
  background: #fff;
  filter: var(--drop-shadow);
  margin: var(--mobile-gutters);
  border-radius: var(--border-containers);
}
</style>