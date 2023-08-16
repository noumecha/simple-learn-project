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