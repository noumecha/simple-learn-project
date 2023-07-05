<!-- eslint-disable vue/multi-word-component-names -->
<template>
    <div class="exo-container">
        <h1>Tringering Vue methods</h1>
        <ul class="links-container">
            <li v-for="index in 7" :key="index">
                <a class="tmc-link" @click="triggerAlert(index)"> Click to claim {{ index}} </a>
            </li>
        </ul>
    </div>
</template>
<script setup>
    const triggerAlert = (index) => {
        alert(`${index} has been claimed`)
    }
</script>
<style>
    .exo-container {
        display: flex;
        width: 100%;
        padding: 20px;
        flex-direction: column;
        align-items: center;
        justify-content: center;
    }
    .links-container {
        display: flex;
        width: 100%;
        padding: 10px;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }
    .links-container li {
        list-style-type: none;
        padding: 10px;
        margin-bottom: 10px;
    }
    .interests-link > ol > li {
        font-size: 16px;
    }
    .tmc-link {
        width: auto;
        height: auto;
        padding: 10px 20px;
        background-color: #04BF37;
        color: white;
        text-decoration: none;
        margin-bottom: 20px;
        border: 1px solid #04BF37;
        cursor: pointer;
    }
    a {
        font-size: 16px;
    }
</style>