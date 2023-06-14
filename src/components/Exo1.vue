<!-- eslint-disable vue/multi-word-component-names -->
<template>
    <div class="app">
        <logo/>
        <h2>
            {{  isUppercase ? title.toUpperCase() : title }}
            <!-- {{  title.toUpperCase() }} -->
        </h2>
        <p>
            this is a simple vue component for understanding
            the basics!
        </p>
        <h3> {{ "VUE-JS | V-TEXT DIRECTIVE".toUpperCase() }} </h3>
        <p v-text="msg"></p>
        <h3> {{ "VUE-JS | V-ONCE DIRECTIVE".toUpperCase() }} </h3>
        <p v-once>this directive render the attribute and its children exactly once</p>
        <h3> {{ "VUE-JS | V-HTML DIRECTIVE".toUpperCase() }} </h3>
        <div v-html="html_element"></div>
        <h3> {{ "VUE-JS | V-BIND DIRECTIVE".toUpperCase() }} </h3>
        <img :src="tmc" width="90" height="90"/><!-- we can also use v-bind:src -->
        <h3> {{ "VUE-JS | V-show DIRECTIVE".toUpperCase() }} </h3>
        <p id="el" v-show="true">This message is hidden by default!</p>
        <code>
            Dev : {{  author.toUpperCase() }}
        </code>
    </div>
</template>

<script setup>
    import logo from "./logo.vue"
    import tmc from '../assets/tmc.png'
    const author = "noumel"
    const html_element = "<p>the value passed v-html directive is render as a valid html el.But it is not recommended to use v-html on client side</p>"
    const msg = "Soft vue learning"
    const title = "My First Vue 3 component"
    const isUppercase = true
/*export default {
    data() {
        return {
            author : "John"
        }
    }
}*/
</script>

<style>
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
        border-radius: 20px;
        padding: 20px;
        widows: 100%;
        background-color: white;
        color: black;
    }
    .app div, p {
        margin-bottom: 20px;
    }
</style>