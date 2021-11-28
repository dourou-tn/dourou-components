<template>
<a
  v-text="text"
  :href="href"
  v-on="$listeners"
  class="inline-block align-baseline text-purple hover:text-indigo-500"
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
