<script setup lang="ts">
import { ref } from 'vue';
import type { VDataTableHeader } from '@gits-id/table';

const states = ['active', 'inactive'];

const items = [...Array(30)].map((_, index) => ({
  index,
  name: `User-${index}`,
  email: `user-${index}@example.com`,
  age: index + 1 * 10,
  state: states[Math.floor(Math.random() * states.length)],
}));

const headers = ref<VDataTableHeader[]>([
  {
    value: 'index',
    text: 'ID',
  },
  {
    value: 'name',
    text: 'Name',
  },
  {
    value: 'email',
    text: 'Email',
  },
  {
    value: 'age',
    text: 'Age',
  },
]);
</script>

<template>
  <!-- VDataTable is registered globally -->
  <div class="mt-[2.5rem] w-3/4 mx-auto">
    <VDataTable :items="items" :headers="headers" />
  </div>
</template>
