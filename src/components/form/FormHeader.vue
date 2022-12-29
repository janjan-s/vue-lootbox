<template>
    <nav class="header">
        <ul>
            <li class="selected"><h2>Add new item</h2></li>
            <li><h2>Global Settings</h2></li>
        </ul>
    </nav>
</template>


<script lang="ts">
import { defineComponent } from "@vue/runtime-core";

export default defineComponent({
    name: 'FormHeader'
})

</script>


<style scoped>

ul {
    list-style-type: none;
    display: flex;
    padding: 0;
    text-align: left;
}

li {
    flex: 1 1 50%;
    background: var(--purple);
    margin-top: -16px;
    height: 5em;
    line-height: 5em;
    /* vertical-align: middle; */
}

li:nth-child(1) {
    border-top-left-radius: var(--border-containers);
}


li:nth-child(2) {
    border-top-right-radius: var(--border-containers);
}

li:not(.selected) {
    cursor: pointer;
}

li.selected {
    background: #fff;
    cursor: default;
}

li h2 {
    margin-left: 10%;
}

</style>