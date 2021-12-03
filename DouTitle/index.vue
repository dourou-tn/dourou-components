<template>
  <h2 class="text-purple-500 font-bold text-2xl text-center font-medium my-10">
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
  },
}
</script>
