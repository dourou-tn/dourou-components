<template>
<a
  v-text="text"
  :href="href"
  v-on="$listeners"
  class="focus:outline-none focus:ring-2 focus:ring-offset-1 focus:ring-purple-500 font-bold inline-block align-baseline text-purple-500 hover:text-indigo-500"
/>
</template>
<script>
export default {
  name: 'DouHref',
  props: {
    text: {
      type: String,
      required: true
    },
    href: {
      type: String,
      default: '#',
    }
  }
}
</script>
