<!-- eslint-disable vue/multi-word-component-names -->
<template>
    <div class="app">
        <logo class="logo"/>
        <Exo3 />
    </div>
</template>

<script setup>
import Exo3 from './learncomponents/Exo3.vue';
import logo from "./logo.vue"
/*export default {
}*/
</script>

<style>
    .logo {
        margin-bottom: 20px;
    }
    h2,h3 {
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
        padding: 20px;
        widows: 100%;
        background-color: white;
        color: black;
    }
    .app div, p {
        margin-bottom: 20px;
    }
</style>