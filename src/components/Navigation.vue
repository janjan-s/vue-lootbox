<template>
    <nav>
        <ul>
            <li><img src="https://via.placeholder.com/57" alt=""></li>
            <li class="account-widget">
                <img src="https://via.placeholder.com/57" alt="">
                <p>Alex Traier</p>
            </li>
        </ul>
        </nav>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
    name: 'Navigation',
})
</script>

<style scoped>

nav ul  {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    list-style-type: none;
    margin-top: 15px;
    padding: 0;
}

.account-widget {
    background: var(--white);
    border-radius: var(--border-containers);
    filter: var(--drop-shadow);
    display: flex;
    flex-direction: row;
    width: 45%;
    font-size: var(--text-mobile-title);
    font-weight: bold;
}

.account-widget img {
    /* position: absolute; */
    margin-left: -20px;
    margin-right: 5px;
}

.account-widget p {
    width: 20px;
    line-height: 1.0;
    margin: auto 0;
}

img {
    border-radius: 50%;
}

@media screen and (min-width: 768px) {
    .account-widget {
        width: 20%;
    }
}

</style>