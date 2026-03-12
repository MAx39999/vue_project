<script setup>
import Button from '../basic/Button.vue';
import LocationIcon from '../icons/LocationIcon.vue';
import { ref } from 'vue';

const isEditing = ref(false)
const city = ref('')
const emit = defineEmits(['select-city'])

function save() {
  emit("select-city", city.value)
  isEditing.value = false
}
</script>

<template>
    <Button class="test" v-if="!isEditing" text="Изменить город" @click="isEditing = true">
        <LocationIcon />
    </Button>
    <template v-else>
        <input v-model="city" placeholder="Введите город" />
        <Button text="Сохранить" @click="isEditing = false" />
    </template>
</template>

<style scoped></style>
