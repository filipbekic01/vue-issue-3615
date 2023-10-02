<script setup lang="ts" generic="T extends string | undefined | null">
defineProps<{
  modelValue: T;
}>();

const emit = defineEmits<{
  (e: "update:model-value", modelValue: T): void;
}>();
</script>

<template>
  <input
    type="text"
    :model-value="modelValue"
    @input="(e) => emit('update:model-value', e)"
  />
</template>
