<!-- ChildComponent1.vue -->
<template>
  <div>
    <h4>Child one</h4>
    <input
      type="text"
      :value="nodeOne"
      @input="updateModelName1($event.target.value)"
    />
  </div>
</template>

<script setup lang="ts">
import { defineProps, defineEmits, ref } from 'vue';

const props = defineProps({
  nodeOne: {
    type: String,
    default: '',
  },
});

const emit = defineEmits<{
  (e: 'update:nodeOne', value: string): void;
}>();

function updateModelName1(newValue: string) {
  emit('update:nodeOne', newValue);
}
</script>
