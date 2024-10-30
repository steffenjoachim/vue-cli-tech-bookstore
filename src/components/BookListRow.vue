<template>
  <tr class="table-item__table-row">
    <td>{{ book.title }}</td>
    <td>{{ book.isbn }}</td>
    <td><base-button text="Add Bookmark" buttonStyle="btn--secondary"/></td>
  </tr>
</template>

<script>
import BaseButton from './BaseButton.vue';

export default {
  components: {
    BaseButton,
  },
  props: {
    book: Object,
  },

};
</script>

<style scoped>
.table-item__table td {
  padding: 12px 15px;
}
.btn {
  border: 3px solid transparent;
  border-radius: 3px;
  padding: 5px;
  cursor: pointer;
}

.btn--primary {
  border-color: var(--primary-dark);
  background-color: var(--primary);
  color: #fff;
}

.btn--primary:hover {
  border-color: var(--primary);
  background-color: var(--primary-dark);
}

.btn--secondary {
  border-color: var(--primary);
  background-color: transparent;
  color: var(--primary);
}

.btn--secondary:hover {
  background-color: var(--primary);
  color: #fff;
}
</style>
