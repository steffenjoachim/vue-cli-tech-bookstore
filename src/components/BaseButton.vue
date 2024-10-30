<template>
    <button :class="['btn', buttonStyle]"
            @click="toggleBookmarked">
            {{  text }}
    </button>
  </template>
<script>
export default {
  props: {
    buttonStyle: {
      type: String,
      default: 'btn--primary',
    },
    text: String,
  },
  emits: ['toggleBookmarked'],
  methods: {
    toggleBookmarked() {
      this.$emit('toggleBookmarked');
    },
  },
};
</script>
