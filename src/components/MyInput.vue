<template>
  <input
    type="text"
    :value="modelValue"
    @input="emit('update:model-value', 'dwq')"
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
