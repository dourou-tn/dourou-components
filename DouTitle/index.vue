<template>
  <h2
    :class="`text-${color}`"
    class="font-semibold text-2xl md:text-3xl text-center my-14 text-purple-500">
    {{ text }}
  </h2>
</template>

<script>
export default {
  name: 'DouTitle',
  props: {
    text: {
      type: String,
      required: true,
    },
    color: {
      type: String,
      default: 'purple-500',
    },
  },
}
</script>
