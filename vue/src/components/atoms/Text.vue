<template>
  <div>
    <label :htmlFor="fieldData.name">{{ fieldData.label }}</label>
    <input
      :type="fieldData.fieldType.toLowerCase()"
      :name="fieldData.name"
      :id="fieldData.name"
      :placeholder="fieldData.placeholder"
    />
  </div>
</template>

<script setup lang="ts">
import { FieldType } from "../../types";
const { fieldData } = defineProps<FieldType>();
</script>
