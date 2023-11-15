<script setup lang="ts">
const { data } = await useFetch<any>('/api/jokes/recent')
</script>

<template>
  <div>
    Hey Köln!
    <Icon style="font-size: 100pt;" name="heroicons:academic-cap" />
    <ul>
      <li v-for="joke in data">
        {{ joke!.joke }}
      </li>
    </ul>
  </div>
</template>
