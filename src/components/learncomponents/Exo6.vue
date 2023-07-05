<!-- eslint-disable vue/multi-word-component-names -->
<template>
    <div class="exo-container">
        <h1>Specials Interests</h1>
        <ul class="links-container">
            <li class="interests-link" v-for="(item, n) in interests" :key="n">
                {{  item.title }}
                <ol v-if="item.favorites.length > 0">
                    <li v-for="(fav, f) in item.favorites" :key="f">
                        {{ fav }}
                    </li>
                </ol>
            </li>
        </ul>
    </div>
</template>
<script setup>
    const interests = [
        {
            title : "RAP",
            favorites : ["Youssoupha","2Pac"]
        },
        {
            title : "Games",
            favorites : ["Fifa","COD","Adventure"]
        },
        {
            title : "Sports",
            favorites : ["Football","Basketball"]
        },
        {
            title : "Books",
            favorites : []
        }
    ];
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