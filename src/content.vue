<template>
  <div class="content">
    <slot></slot>
  </div>
</template>

<script>
  export default {
    name: "z-content"
  }
</script>

<style scoped lang="scss">
  .content{
    flex-grow: 1;
    background: #eee;
  }
</style>