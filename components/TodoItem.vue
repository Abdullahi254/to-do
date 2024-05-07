<template>
  <li @click.prevent="rule" :class="strike ? 'line-through cursor-pointer': 'cursor-pointer'">
    {{ item }}
  </li>
</template>

<script lang="ts" setup>
  const strike = ref(false)
  const rule = ()=>{
    strike.value = !strike.value
  }
  const props = defineProps(['item'])
</script>

<style>

</style>