<!-- ParentComponent.vue -->
<template>
  <div>
    <h1>Multi-Comp-2Ways</h1>
    <ChildOne v-model:nodeOne="sharedData" />
    <ChildTwo v-model:nodeTwo="sharedData" />

    <div>
      <h2>Parent</h2>
      {{ sharedData }}
    </div>
  </div>
</template>

<script setup lang="ts">
//<ChildTwo v-model:name2="sharedData" />
import { ref } from 'vue';
import ChildOne from './ChildOne.vue';
import ChildTwo from './ChildTwo.vue';

const sharedData = ref('Hello from parent name');
</script>
