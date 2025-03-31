<script setup lang="ts">
import { CheckboxGroupRoot, CheckboxRoot } from 'reka-ui';

const fruits: string[] = []
</script>

<template>
  <form @submit.prevent="console.log('submit')">
    <CheckboxGroupRoot v-model="fruits">
      <CheckboxRoot>
        Apple
      </CheckboxRoot>
      
      <CheckboxRoot>
        Banana
      </CheckboxRoot>
      
      <CheckboxRoot>
        Cherry
      </CheckboxRoot>
    </CheckboxGroupRoot>

    <button type="submit">Submit</button>
  </form>
</template>

<style scoped>
</style>
