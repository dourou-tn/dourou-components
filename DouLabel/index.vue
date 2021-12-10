<template>
  <label
    :class="`text-${color}`"
    class="label block text-sm font-bold mb-2"
    for="username"
  >
    {{ label }}
  </label>
</template>

<script>
  export default {
    name: 'DouInput',
    props: {
      label: {
        type: String,
        required: true
      },
      color: {
        type: String,
        default: 'purple-500'
      }
    }
  }
</script>
