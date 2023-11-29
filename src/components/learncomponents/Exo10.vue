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
        /*beforeCreate() {
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
        }*/
    }
</script>
<style>
</style>