<script setup>
const props = defineProps({
  word: {
    type: String,
    required: true
  },
  isFlipped: {
    type: Boolean,
    required: true
  }
})
const emit = defineEmits(['flip', 'change-status'])
</script>

<template>
    <div class="card-wrapper">
        <div class="card">
            <span class="number">01</span>
            <div class="word">{{ word }}</div>
            <button class="flip-btn" @click="emit('flip')">ПЕРЕВЕРНУТЬ</button>
        </div>
    </div>
</template>

<style scoped>
.card-wrapper {
    background: var(--color-accent);
    padding: 3px;
    border-radius: 20px;
}

.card {
    background: var(--color-bg);
    border-radius: 18px;
    padding: 24px;
    min-width: 260px;
    min-height: 400px;
    display: flex;
    flex-direction: column;
    align-items: center;
    position: relative;
    border: 1px solid var(--color-accent);
}

.number {
    position: absolute;
    top: 16px;
    left: 20px;
    font-size: 14px;
    color: #999;
}

.word {
    flex: 1;
    display: flex;
    align-items: center;
    font-size: 22px;
    color: var(--color-text);
}

.flip-btn {
    background: none;
    border: none;
    cursor: pointer;
    font-weight: 700;
    font-size: 13px;
    letter-spacing: 1.5px;
    color: var(--color-text);
    padding: 8px;
}
</style>
