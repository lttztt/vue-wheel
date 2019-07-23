<template>
  <div class="toast">
    <slot></slot>
  </div>
</template>

<script>
  export default {
    name: "z-toast",
    props: {
      autoClose: {
        type: Boolean,
        default: true
      },
      autoCloseDelay: {
        type: Number,
        default: 3
      }
    },
    mounted() {
      let {autoClose, close, autoCloseDelay} = this;
      if (autoClose) {
        setTimeout(() => {
          close();
        }, autoCloseDelay * 1000)
      }
    },
    methods: {
      close(){
        this.$el.remove();
        this.$destroy()
      }
    }
  }
</script>

<style scoped lang="scss">
  $font-size: 14px;
  $toast-min-height: 40px;
  $toast-bg: rgba(0, 0, 0, 0.75);
  .toast {
    position: fixed;
    top: 0;
    left: 50%;
    transform: translateX(-50%);
    font-size: $font-size;
    min-height: $toast-min-height;
    display: flex;
    line-height: 1.8;
    color: white;
    align-items: center;
    background: $toast-bg;
    border-radius: 4px;
    box-shadow: 0 0 3px 0 rgba(0, 0, 0, 0.50);
    padding: 0 16px;
  }
</style>