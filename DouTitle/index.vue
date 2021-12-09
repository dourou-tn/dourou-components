<template>
  <h2
    :class="`text-${color}`"
    class="font-bold text-2xl text-center font-medium my-10">
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
