<template>
  <div class="header">
    <slot></slot>
  </div>
</template>

<script>
  export default {
    name: "z-header"
  }
</script>

<style scoped>
  .header{
    background-color: gray;
  }
</style>