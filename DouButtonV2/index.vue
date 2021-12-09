<template>
  <button
    v-bind="$attrs"
    v-on="$listeners"
    :class="`border-${color}-500 hover:border-${color}-600 hover:bg-${color}-500 `"
    class="bg-white text-gray-800 font-bold rounded border-b-2 hover:text-white shadow-md py-2 px-6 inline-flex items-center">
    <span class="mr-2">{{ label }}</span>
    <slot></slot>
  </button>
</template>
<script>
export default {
  name: 'DouButtonV2',
  props: {
    label: { type: String, default: '' },
    color: { type: String, default: 'purple' },
  }
}
</script>