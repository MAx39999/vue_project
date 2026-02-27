<script setup>
import { ref } from 'vue'
let text = ref('');
</script>

<template>
    <header>
    </header>
    <main>
        <input :value="text" @input="text = $event.target.value" />
        <p>{{ text }}</p>
    </main>
    <footer>
    </footer>
</template>

<style scoped></style>
