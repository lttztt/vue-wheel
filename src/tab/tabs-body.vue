<template>
  <div class="tabs-body">
    <slot></slot>
  </div>
</template>

<script>
  export default {
    name: "z-tabs-body",
    inject: ['eventBus'],
    created() {
    }
  }
</script>

<style scoped>
  .tabs-body{
    padding: 1em;
  }
</style>