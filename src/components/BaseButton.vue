<template>
    <button :class="['btn', buttonStyle]">{{  text }}</button>
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
};
</script>
