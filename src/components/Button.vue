<script setup>
</script>

<template>
    <button class="button">
        <div>
            <slot name="text" />
        </div>
    </button>
</template>

<style scoped>
.button {
    border: none;
    border-radius: 40px;
    background: var(--background);
    font-size: 20px;
    font-weight: 400;
    color: var(--color-primary);
    width: 335px;
    height: 68px;
    padding: auto;
}
</style>
