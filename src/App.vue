<script setup>
import { ref } from 'vue'
import Header from './components/composite/Header.vue';
import Card from './components/basic/Card.vue';
const score = ref(100)
const isFlipped = ref()
const word = ref()
</script>

<template>
    <Header :score="score" />
    <main class="main">
        <Card :word="word" :isFlipped="isFlipped"></Card>
    </main>
</template>

<style scoped>
.main {
    display: flex;
    justify-content: center;
    padding: 60px 50px;
}
</style>

