<!-- eslint-disable vue/multi-word-component-names -->
<template>
    <div class="exo-container">
        <h1>Looping through object properties</h1>
        <div class="interests-link" v-for="(value, key) in information" :key="key">
            {{ key }} : {{ value.toString() }}
        </div>
    </div>
</template>
<script setup>
const information = {
    title: "List of vue js concepts",
    subtitle: "Vue JS basics",
    items: ["Looping", "Data", "Methods","Directives"]
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
    .interests-link {
        list-style-type: none;
        padding: 10px;
        margin-bottom: 10px;
        width: 100%;
        background: rgb(0, 0, 0);
        color: white;
        font-size: 22px;
        border-radius: 15px;
        display: block;
    }
    .interests-link > ol > li {
        font-size: 16px;
    }
</style>