<template>
<div class="modal" :class="show ? 'modal-open' : ''">
  <div
    class="modal-box max-w-xl"
  >
    <slot />
  </div>
</div>
</template>

<script>
export default {
  name: 'DouModal',
  props: {
    show: {
      type: Boolean,
      default: false,
    }
  }
}
</script>
