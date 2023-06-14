<!-- eslint-disable vue/multi-word-component-names -->
<template>
    <div class="exo">
        <h1  class="title" v-show="true" v-once v-text="text"></h1>
        <h2 v-show="false" v-html="html"></h2>
        <a
            class="tmc-link"
            :href="link.url"
            :target="link.target"
            :title="link.title"
            :tabindex="link.tabindex"
        >
            {{ link.title }}
        </a>
    </div>
</template>

<script setup>
    const text = "Directive text";
    const html = 'Stylise<br/>HTML in<br/><b>your data</b>'
    const link = {
        url : "https://github.com/noumecha",
        target : "_blank",
        title : "Click Me",
        tabindex : 7
    }
</script>

<style>
    .exo {
        display: flex;
        flex-direction: column;
        align-items: center;
        background: black;
        padding: 20px;
        border-radius: 20px;
        width: 100%;
    }
    .title {
        margin-bottom: 20px;
        color: white;
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
    }
    .tmc-link:hover {
        backdrop-filter: white;
        color: #04BF37;
    }
</style>