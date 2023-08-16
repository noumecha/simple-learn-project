<!-- eslint-disable vue/multi-word-component-names -->
<template>
    <div class="exo-container">
        <h1>Vue lifecycle Hooks</h1>
        <ul class="links-container">
            <li v-for="(item, n) in list" :key="n">
                <div>{{ item }}</div>
                <a class="tmc-link" type="button" @click="deleteItem(item)">
                    Delete
                </a>
            </li>
        </ul>
    </div>
</template>
<script>
    export default {
        data() {
            return {
                list: [
                    'Street Art',
                    'Hip Hop attitude',
                    'RAP Kulture',
                    'Africa History',
                    'Black live matters',
                    'Segregation',
                    'Africans Genocides',
                    'Testing unmounted hooks'
                ],
            }
        },
        methods: {
            deleteItem(i) {
                this.list = this.list.filter(item => item !== i)
            }
        },
        beforeCreate() {
            alert("beforeCreate: data is static, thats it")
        },
        created() {
            alert("created: data and events ready, but no DOM")
        },
        beforeMount() {
            alert(`beforeMount: $el not ready`)
        },
        mounted() {
            alert(`mounted: data ready to use`)
        },
        beforeUpdate() {
            alert("beforeUpdate: we know an update is about happen, and have the data")
        },
        updated() {
            alert("updated: virtual DOM will update after we Click ON")
        },
        beforeUnmount() {
            alert("beforeUnmount: about a blow up this component")
        },
        unmounted() {
            alert("unmounted: this component has been destroyed")
        }
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
        width: 100%;
        display: flex;
        align-items: center;
        justify-content: space-between;
        list-style-type: none;
        padding: 10px;
        margin: 0;
    }
    .links-container li div {
        width: auto;
        height: auto;
        padding: 10px 20px;
        margin: 0;
    }
    .interests-link > ol > li {
        font-size: 16px;
    }
    .tmc-link {
        width: auto;
        height: auto;
        padding: 10px 20px;
        margin: 0;
        background-color: red;
        color: white;
        text-decoration: none;
        border: 1px solid red;
        cursor: pointer;
    }
    .tmc-link:hover {
        color: red;
        background: white;
    }
    a {
        font-size: 16px;
    }
</style>