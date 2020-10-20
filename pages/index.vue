<template>
  <div class="wrapper">
    <h1 class="text-4xl uppercase">nuxt-app</h1>
  </div>
</template>

<script>
import { default as Routes } from '@/utils/routes'
export default {
  mounted() {
    console.log('pages', Routes )
  },
}
</script>

<style>
/* Sample `apply` at-rules with Tailwind CSS
.container {
@apply min-h-screen flex justify-center items-center text-center mx-auto;
}
*/
</style>

<style scoped>
.wrapper {
  height: 100vh;
  background: #dedede;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
