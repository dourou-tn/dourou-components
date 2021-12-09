<template>
  <button
    :class="`bg-${color}`"
    class=" hover:bg-indigo-700 text-white py-2 px-4 rounded focus:outline-none focus:shadow-outline" type="button"
    v-on="$listeners"
  >
    {{ label }}
  </button>
</template>
<script>
export default {
  name: 'DouButton',
  props: {
    label: {
      type: String,
      required: true
    },
    color: {
      type: String,
      default: 'purple-500',
    }
  }
}
</script>