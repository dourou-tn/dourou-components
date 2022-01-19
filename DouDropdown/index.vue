<template>
  <div class="relative inline-block">
    <div>
      <span class="text-sm text-orange-500 cursor-pointer hover:opacity-80" @click="openMenu" :class="{ 'opacity-80': isOpen }">{{ activator }}<span class="text-white">, connecté</span></span>
    </div>

    <div v-if="isOpen" v-click-outside="closeMenu" class="origin-top-right absolute right-0 mt-2 w-56 rounded-md shadow-lg bg-white ring-1 ring-black ring-opacity-5 focus:outline-none" role="menu" aria-orientation="vertical" aria-labelledby="menu-button" tabindex="-1">
      <div class="py-1" role="none">
        <slot name="menu" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'DouDropdown',
  props: {
    activator: {
      type: String,
      required: true,
    },
  },
  data() {
    return {
      isOpen: false,
    }
  },
  methods: {
    openMenu (e) {
      e.stopPropagation();
      this.isOpen = !this.isOpen;
    },
    closeMenu () {
      this.isOpen = false;
    }
  }
}
</script>