<template>
  <span role="button" @click="select">
    <slot :selected="selected" />
  </span>
</template>
<script setup lang="ts">
import { computed } from 'vue';
import { useTabs } from './BaseTabs.vue';

const props = defineProps<{ index: number }>();

const { selectedIndex } = useTabs();
const selected = computed(() => selectedIndex.value === props.index);

function select() {
  selectedIndex.value = props.index;
}
</script>
