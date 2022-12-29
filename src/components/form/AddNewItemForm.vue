<template>
    <form class="content">
        <div class="form-control">
            <label for="item-name">Item Name</label>
            <input class="text" name="item-name" type="text">
        </div>
        <div class="form-control">
            <label for="item-description">Item Description</label>
            <input class="text-area text" name="item-description" type="text">
        </div>
        <div class="form-control">
            <label for="item-image">Upload image</label>
            <input name="item-image" type="file">
        </div>

        <AppButton />
    </form>
</template>


<script lang="ts" setup>
import AppButton from '../blocks/AppButton.vue'

</script>

<script lang="ts">
import { defineComponent } from "@vue/runtime-core";

export default defineComponent({
    name: 'AddNewItemForm'
})
</script>

<style scoped>



</style>