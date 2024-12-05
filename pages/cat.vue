<script setup lang="ts">
import Cat from '../components/Cat.vue'

const { data } = useAsyncData<number>('ss', async () => {
  return new Promise<number>((resolve, reject) => {
    setTimeout(() => resolve(2), 100)
  })
})
</script>

<template>
  <div class="page">
    <Cat :data="data" />
  </div>
</template>
