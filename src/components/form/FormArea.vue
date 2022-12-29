<template>
    <section class="content">
        <FormHeader />
        <form>
            <label for="item-name">Item Name</label>
            <input name="item-name" type="text">
            <input type="file">
            <AppButton />
        </form>

    </section>
</template>

<script setup lang="ts">
import AppButton from '../blocks/AppButton.vue'
import FormHeader from './FormHeader.vue'

</script>

<script lang="ts">
import { defineComponent } from "@vue/runtime-core";

export default defineComponent({
    name: 'FormArea',
})

</script>


<style scoped>

section {
  background: #fff;
  filter: var(--drop-shadow);
  margin: var(--mobile-gutters);
  border-radius: var(--border-containers);
  padding-top: 1em;
}

@media screen and (min-width: 1200px) {
    section {
        width: 30%
    }
}

</style>