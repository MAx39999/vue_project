<script setup>

import CitySelect from './components/composite/CitySelect.vue';
import Stat from './components/basic/Stat.vue';
const data = {
    label: "Влажность",
    stat: "90%"
}

function getCity(city) {
    console.log(city)
}
</script>

<template>
    <header>
    </header>
    <main class="main">
        <Stat v-bind="data" />
        <Stat label="Осадки" stat="0%" />
        <Stat label="Ветер" stat="3 м/c" />

        <CitySelect @select-city="getCity" />

    </main>
    <footer>
    </footer>
</template>

<style scoped>
.main {
    background: var(--color-bg-main);
    padding: 60px 50px;
    border-radius: 25px;
}
</style>
