<script setup lang="ts">
import { useCryptoStore } from './store/crypto'

const props = useCryptoStore()

// https://github.com/vueuse/head
// you can use this to manipulate the document head in any components,
// they will be rendered correctly in the html results with vite-ssg
useHead({
  title: 'Pongtorn Sangkaphet Project',
  meta: [
    { name: 'description', content: 'Crypto Project' },
  ],
})

</script>

<template>
  {{ props.loading }}
  <Loader v-if="props.loading" />
  <router-view />
</template>
