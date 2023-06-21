<!-- eslint-disable vue/multi-word-component-names -->
<template>
    <h1>Looping through arrays</h1>
    <ul>
        <li v-for="(interest, index) in interests" :key="index">
            {{ interest }}
        </li>
    </ul>
    <h1>Learns Objects</h1>
    <ul>
        <li v-for="learn in learns" :key="learn.id">
            <h2>{{ learn.title }}</h2>
            <h3>duration : {{ learn.min_duration }}</h3>
            <h3>state : {{ learn.state }}</h3>
            <h3>Main concepts : </h3>
            <ul>
                <li v-for="(mc, index) in learn.main_concepts" :key="index">
                    <span>{{ mc }}</span>
                </li>
            </ul>
        </li>
    </ul>
</template>

<script setup>
    const interests = [
        'Books',
        'Games',
        'Sports',
        'RAP',
        'Cybersecurity',
        'Coding',
        'Drawing',
        'Poetry',
        'Music',
        'Tech-tools',
        'Scientific facts',
        'Entrepreneurship',
        'X-treme tricks',
        'Travel'
    ];
    const learns = [
        {
            id: 1,
            title: "JAVA",
            min_duration: "2 months",
            state: "50%",
            main_concepts: ['UI','API','Syntax','Classes']
        },
        {
            id: 2,
            title: "PYTHON",
            min_duration: "2 months",
            state: "70%",
            main_concepts: ['UI','ML','API','Syntax']
        },
        {
            id: 3,
            title: "LARAVEL",
            min_duration: "3 months",
            state: "60%",
            main_concepts: ['UI','API','Syntax','Databases']
        }
    ];
</script>

<style>
    h2 {
        margin-bottom: 10px;
    }
</style>