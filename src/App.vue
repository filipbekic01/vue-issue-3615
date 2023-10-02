<script setup lang="ts">
import { ref } from 'vue';

const name = ref('test');
</script>

<template>
 <MyInput :model-value="name" @update:model-value="(e) => name = e"/>
</template>
