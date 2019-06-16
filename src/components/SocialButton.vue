<template>
  <v-btn
    class="mx-3"
    icon
  >
    <a v-bind:href="iconLink" class="link" target="_blank">
      <v-icon size="24px">{{ icon }}</v-icon>
    </a>
  </v-btn>
</template>

<script>
export default {
  props: ['icon', 'iconLink']
}
</script>

<style scoped>
  .link {
    color: #1B1E1E;
  }
</style>
