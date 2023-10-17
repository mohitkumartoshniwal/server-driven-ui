<template>
  <Generator :schema="schema" />
</template>

<script setup lang="ts">
import { onMounted, ref } from "vue";
import { SchemaType } from "./types";

import Generator from "./components/Generator.vue";
const schema = ref<SchemaType[]>([]);

onMounted(() => {
  fetch(`http://localhost:3000/schema`)
    .then((response) => response.json())
    .then((schemaData) => (schema.value = schemaData));
});
</script>
