<template>
  <label
    class="block text-purple text-sm font-bold mb-2"
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
      }
    }
  }
</script>
