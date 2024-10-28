<template>
    <button :class="['btn', buttonStyle]">{{  text }}</button>
  </template>
<script>
export default {
  name: 'BaseButton',
  props: {
    buttonStyle: {
      type: String,
      default: 'btn--primary',
    },
    text: String,
  },
};
</script>
