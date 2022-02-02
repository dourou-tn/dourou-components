<template>
  <button
    :class="`bg-${color} text-${textColor} focus:outline-${textColor}`"
    class="text-sm shadow hover:shadow-lg py-2 px-4 rounded focus:outline-none focus:ring-2 focus:ring-offset-1 focus:ring-purple-600 font-bold hover:opacity-90" type="button"
    v-on="$listeners"
    v-bind="$attrs"
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
    },
    textColor: {
      type: String,
      default: 'orange-500',
    },
  }
}
</script>