<template>
    <div>
        <span> > </span>
        <span> &lt; </span>
    </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
    name: 'Arrows',
})
</script>

<style scoped>
div {
    position: absolute;
    right: 2.5%;
    top: 15%;
    display: flex;
    flex-direction: column;
    margin: auto;
}

div span {
    border-radius: 40%;
    background: blue;
    width: 64.5px;
    height: 82.5px;
    text-align: center;
    color: #fff;
    font-size: 2em;
    line-height: 2.6;
    cursor: pointer;
}

div span:first-child {
    margin-bottom: 1em;
}

@media screen and (min-width: 992px) {
    div {
        display: none;
    }

}

</style>