<template>
  <div class="grid gap-4 sm:gap-5 lg:gap-6 grid-cols-1 sm:grid-cols-2 md:grid-cols-2 lg:grid-cols-2 xl:grid-cols-2">
    <slot />
  </div>
</template>
<script>
export default {
  name: 'DouGrid',
}
</script>
