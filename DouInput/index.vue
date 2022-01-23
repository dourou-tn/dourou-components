<template>
  <div class="form-control">
    <DouLabel v-if="label" :label="label" :color="dark ? 'white' : 'purple-500'" />
    <input
      class="shadow appearance-none border border-purple-400 rounded w-full py-2 px-3 leading-tight focus:outline-none focus:ring-1 focus:ring-offset-0 focus:ring-purple-500 bg-purple-200"
      :class="{ 'border-red-300': error, 'bg-neutral': dark, 'text-white': dark, 'text-gray-700': !dark }"
      :id="id"
      :type="type"
      :placeholder="placeholder"
      v-bind="$attrs"
      v-on="inputListeners"
      :value="value"
    />
    <p v-if="hint" v-text="hint" class="text-gray-500 text-xs mt-2" />
    <p v-if="error" v-text="error" class="text-red-500 text-xs mt-2" />
  </div>
</template>

<script>
import DouLabel from '../DouLabel/index.vue';

export default {
  name: 'DouInput',
  components: { DouLabel },
  props: {
    value: {},
    type: {
      type: String,
      default: 'text',
    },
    id: {
      type: String,
    },
    placeholder: {
      type: String,
    },
    label: {
      type: String,
    },
    hint: {
      type: String,
    },
    error: {
      type: String,
      default: '',
    },
    dark: {
      type: Boolean,
      default: false
    }
  },
  computed: {
    inputListeners: function () {
      let vm = this;
      return Object.assign(
         {},
         this.$listeners,
         {
           input: function(e) {
             vm.$emit('input', e.target.value);
           }
         }
      )
    }
  }
}
</script>