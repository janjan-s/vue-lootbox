<template>
    <form class="content">
        <div class="form-control">
            <label for="prize-amount">Amount of prizes</label>
            <input class="number" name="prize-amount" type="number">
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
    name: 'GlobalSettingsForm'
})
</script>

<style scoped>



</style>