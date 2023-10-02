<template>
  <input type="text" v-model="localModel" />
</template>

<script setup lang="ts" generic="T extends string | number">
import { computed } from "vue";

const props = defineProps<{
  modelValue: T;
}>();

const emit = defineEmits<{
  (e: "update:model-value", value: T): void;
}>();

const localModel = computed({
  get: () => props.modelValue,
  set: (value: T) => emit("update:model-value", value),
});
</script>
