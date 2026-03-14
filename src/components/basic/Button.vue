<script setup>
const props = defineProps({
  score: {
    type: Number,
    required: true,
    }
  }
)
</script>

<template>
    <button class="button">
        <div class="text">{{ score }}</div>
        <slot />
    </button>
</template>

<style scoped>
.button {
    border: none;
    border-radius: 36px;
    background: var(--color-accent);
    font-size: 16px;
    font-weight: 700;
    color: var(--color-primary);
    padding: 6px 16px;
    display: flex;
    align-items: center;
    gap: 6px;
    cursor: pointer;
}
</style>
