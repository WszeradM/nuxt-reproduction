<script setup lang="ts">
import { useId } from 'vue'

const id = useId()

defineProps<{ data: number | null }>()
</script>

<template>
<span :id="id">
  {{ data }}
</span>
</template>
