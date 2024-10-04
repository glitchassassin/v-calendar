<template>
  <div>
    <DateDisplay v-model="date">
      <template #default="{ togglePopover }">
        <span
          role="button"
          class="px-3 py-2 bg-blue-500 hover:bg-blue-600 text-sm text-white font-semibold rounded-md"
          @click="togglePopover"
        >
          Select date
        </span>
      </template>
    </DateDisplay>
  </div>
</template>

<script setup>
import { ref, computed } from 'vue';

const date = ref(new Date());
</script>
