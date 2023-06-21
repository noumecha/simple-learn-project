<!-- eslint-disable vue/multi-word-component-names -->
<template>
    <div class="form">
        <label for="name">
            Name
            <input type="text" v-model="name" name="name">
        </label>
        <label for="pref">
            Preferred JS Style
            <select name="pref" v-model="language">
                <option value="JavaScript">JavaScript</option>
                <option value="TypeScript">TypeScript</option>
                <option value="CoffeeScript">CoffeeScript</option>
                <option value="Dart">Dart</option>
            </select>
        </label>
    </div>
    <ul class="overview">
        <li><strong>Overview</strong></li>
        <li>Name : {{ name }}</li>
        <li>Preference : {{ language }}</li>
    </ul>
</template>
<script>
    export default {
        data () {
            return {
                name: '',
                language: '',
            }
        }
    }
</script>
<style>
    .form {
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        max-width: 800px;
        width: 100%;
        align-items: center;
        padding: 40px 20px;
        border-radius: 10px;
        margin: 0 auto;
        background: #ececec;
    }
    .overview {
        display: flex;
        justify-content: space-evenly;
        flex-direction: column;
        max-width: 300px;
        margin: 40px auto;
        padding: 40px 20px;
        border-radius: 10px;
        border:1px solid #ececec;
    }
    .overview > li {
        list-style: none;
    }
    .overview > li > strong {
        text-decoration: underline;
        font-display: 900 !important;
    }
    .overview > li + li {
        margin-top: 20px;
    }
</style>
