<!-- ChildComponent1.vue -->
<template>
  <div>
    <h4>Child two</h4>
    <input
      type="text"
      :value="nodeTwo"
      @input="updateModelName1($event.target.value)"
    />
  </div>
</template>

<script setup lang="ts">
import { defineProps, defineEmits, ref } from 'vue';

const props = defineProps({
  nodeTwo: {
    type: String,
    default: '',
  },
});

const emit = defineEmits<{
  (e: 'update:nodeTwo', value: string): void;
}>();

function updateModelName1(newValue: string) {
  emit('update:nodeTwo', newValue);
}
</script>
