<template>
  <label>
    <input
      type="checkbox"
      :value="modelValue"
      @input="$emit('update:modelValue', !modelValue)"
    >
    {{ modelValue ? 'Completed!' : 'Mark as completed' }}
  </label>
</template>

<script lang="ts" setup>
const props = defineProps({
  modelValue: { type: Boolean, default: false }
})
defineEmits(['update:modelValue'])

</script>
