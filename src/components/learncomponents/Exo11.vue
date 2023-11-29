<!-- eslint-disable vue/multi-word-component-names -->
<template>
    <div class="exo-container">
        <h1>{{ title }}</h1>
    </div>
</template>
<script>
    export default {
        data() {
            return {
                title : "V-bind CSS components",
                titleStyle : {
                    marginTop : "10px",
                    disPlay : "flex",
                    color : "green"
                }
            }
        }
    }
</script>
<style lang="css" scoped>
    h1 {
        margin-top: v-bind(titleStyle.marginTop);
        display: v-bind(titleStyle.disPlay);
        color : v-bind(titleStyle.color);
    }
</style>