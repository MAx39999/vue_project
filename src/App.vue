<script setup>
import Button from './components/Button.vue';
const currentDate = new Date().toLocaleDateString('ru-RU');
</script>

<template>
    <header>
    </header>
    <main class="main">
        <Button>
            <template #icon> {{ currentDate }} </template>
            <template #text>Изменить город</template>
        </Button>
    </main>
    <footer>
    </footer>
</template>

<style scoped></style>
