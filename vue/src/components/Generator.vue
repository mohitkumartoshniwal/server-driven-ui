<template>
  <component
    v-for="(field, index) in schema"
    :key="index"
    :is="components[field.fieldType]"
    :fieldData="field"
  />
</template>

<script setup lang="ts">
import { GeneratorProps } from "../types";
import Text from "./atoms/Text.vue";
import SelectList from "./atoms/SelectList.vue";

const { schema } = defineProps<GeneratorProps>();

const components: Record<string, any> = {
  Text: Text,
  SelectList: SelectList,
};
</script>
