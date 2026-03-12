<script setup>
defineProps({
    text: String,
});
</script>

<template>
    <button class="button">
        <slot />
        <div class="text">{{ text }}</div>
    </button>
</template>

<style scoped>
.button {
    border: none;
    border-radius: 40px;
    background: var(--gradient);
    font-size: 18px;
    font-weight: 400;
    color: var(--color-primary);
    width: 415px;
    height: 53px;
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 9px;
}

.button:hover {
    background: var(--gradient-inverted)
}
</style>
