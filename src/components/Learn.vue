<!-- eslint-disable vue/multi-word-component-names -->
<template>
    <div class="app">
        <logo class="logo"/>
        <Exo3 />
        <Exo4 />
        <Exo5 />
        <Exo6 />
        <Exo7 />
        <Exo8 />
    </div>
</template>

<script setup>
import Exo3 from './learncomponents/Exo3.vue';
import Exo4 from './learncomponents/Exo4.vue';
import Exo5 from './learncomponents/Exo5.vue';
import Exo6 from './learncomponents/Exo6.vue';
import Exo7 from './learncomponents/Exo7.vue';
import Exo8 from './learncomponents/Exo8.vue';
import logo from "./logo.vue"
/*export default {
}*/
</script>

<style>
    .logo {
        margin-bottom: 20px;
    }
    h2 {
        font-family: 'Avenir', Helvetica, Arial, sans-serif;
        color: #04BF37;
        margin-bottom: 20px;
    }
    .app {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        border: 1px solid white;
        border-radius: 30px;
        padding: 100px;
        max-width: 1024px;
        /*width: 100%;*/
        background-color: white;
        color: black;
    }
    .app div, p {
        margin-bottom: 20px;
    }
</style>