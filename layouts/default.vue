<template>
  <div>
    <Nuxt />
    <template v-if="$nuxt.isOffline">
      <Notification
        title="Network Issue"
        text="It looks like you are offline."
        color="danger"
        icon="wifi_off"
      />
    </template>
  </div>
</template>

<script>
export default {
  name: 'default',
}
</script>

<style>
*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
}
</style>
