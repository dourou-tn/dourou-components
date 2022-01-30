<template>
  <div class="flex items-center justify-center space-x-3 animate-bounce">
    <div>
      <div
        style="border-top-color:transparent"
        class="w-8 h-8 border-4 border-solid rounded-full animate-spin"
        :class="`border-${color}`"
      ></div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'DouLoader',
  props: {
    color: {
      type: String,
      default: 'purple-500'
    }
  }
}
</script>