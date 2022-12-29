<template>
    <section class="content">
        <FormHeader />
        <AddNewItemForm />
        <!-- <GlobalSettingsForm /> -->

    </section>
</template>

<script setup lang="ts">
import FormHeader from './FormHeader.vue'
import AddNewItemForm from './AddNewItemForm.vue';
import GlobalSettingsForm from './GlobalSettingsForm.vue'

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
  overflow: hidden;
  width: 100%;
  /* height: 100%; */
}

@media screen and (min-width: 1200px) {
    section {
        width: 30%;
        margin-top: 20px;
    }
}

</style>