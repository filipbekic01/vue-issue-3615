<template>
  <input
    type="text"
    :value="modelValue"
    @input="(e) =>emit('update:model-value', ( e.target as HTMLInputElement).value as T)"
  />
</template>

<script setup lang="ts" generic="T extends string">
defineProps<{
  modelValue: T;
}>();

const emit = defineEmits<{
  (e: "update:model-value", value: T): void;
}>();
</script>
