<!-- eslint-disable vue/multi-word-component-names -->
<template>
    <div class="exo-container">
        <h1>Returning Data using vue methods</h1>
        <div class="Cart">
            <h4>Cart : ({{ totalItems }})</h4>
            <h3>{{ totalCost }} XAF</h3>
        </div>
        <ul class="links-container">
            <li v-for="n in 5" :key="n">
                <a type="button" class="tmc-link" @click="addToCart(n)">
                    Add {{ formatCurrency(n) }} to cart
                </a>
            </li>
        </ul>
    </div>
</template>
<script>
    export default {
        data() {
            return {
                totalCost: 0,
                totalItems: 0
            };
        },
        methods: {
            addToCart(n) {
                this.totalItems = this.totalItems + 1
                this.totalCost = this.totalCost + n;
            },
            formatCurrency(v) {
                return `XAF ${v.toFixed(2)}`;
            }
        }
    }
</script>
<style>
</style>