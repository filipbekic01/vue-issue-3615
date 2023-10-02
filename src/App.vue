<script setup lang="ts">
import { ref } from "vue";
import MyInput from "./components/MyInput.vue";

const firstName = ref("test");
</script>

<template>
  <MyInput
    :model-value="firstName"
    @update:model-value="(e) => (firstName = e)"
  />
</template>
