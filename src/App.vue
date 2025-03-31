<script setup lang="ts">
import { CheckboxGroupRoot, CheckboxRoot } from 'reka-ui'
import { ref, toRaw } from 'vue'

const options = [
  'Apple',
  'Banana',
  'Cherry',
]

const fruits = ref<string[]>([])
</script>

<template>
  <form 
    class="bg-purple-50"
    @submit.prevent="console.log('submit', toRaw(fruits))"
   >
    <CheckboxGroupRoot v-model="fruits" class="flex gap-x-3" required>
      <CheckboxRoot 
        v-for="option in options" 
        :key="option"
        class="bg-pink-200" 
        :value="option"
      >
        {{ option }}
      </CheckboxRoot>
    </CheckboxGroupRoot>

    <button type="submit" class="mt-8">Submit</button>
  </form>
</template>

<style scoped>
</style>
