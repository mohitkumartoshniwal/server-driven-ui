<template>
  <div>
    <label>{{ fieldData.label }}</label>
    <select :multiple="fieldData.multiple">
      <option v-for="option in fieldData.options" :key="option">
        {{ option }}
      </option>
    </select>
  </div>
</template>

<script setup lang="ts">
import { FieldType } from "../../types";
const { fieldData } = defineProps<FieldType>();
</script>
