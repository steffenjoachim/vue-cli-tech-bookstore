<template>
  <AppHeader />
  <BookList />
</template>

<script>
import AppHeader from '@/components/AppHeader.vue';
import BookList from '@/components/BookList.vue';

export default {
  components: {
    AppHeader,
    BookList,
  },
};
</script>

<style>
 @import url('./global.css');
</style>
