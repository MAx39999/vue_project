<script setup>
import Button from '../basic/Button.vue';
import Heart from '../icons/Heart.vue';

const props = defineProps({
  score: {
    type: Number,
    required: true,
  }
})
</script>

<template>
    <header class="header">
        <div class="text">Запомни слово</div>
        <Button :score="score">
            <Heart />
        </Button>
    </header>
</template>

<style scoped>
.header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    background: var(--color-bg);
    padding: 16px 24px;
    border-bottom: 1px solid #eee;
}

.text {
    color: var(--color-text);
    font-weight: 700;
    font-size: 14px;
    text-transform: uppercase;
    letter-spacing: 0.5px;
}
</style>
