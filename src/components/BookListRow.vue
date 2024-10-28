<template>
  <tr class="table-item__table-row">
    <td>{{ title }}</td>
    <td>{{ isbn }}</td>
    <td><base-button text="Add Bookmark"/></td>
  </tr>
</template>

<script>
import BaseButton from './BaseButton.vue';

export default {
  name: 'BookListRow',
  components: {
    BaseButton,
  },
  props: {
    title: String,
    isbn: Number,
    author: String,
    publischer: String,
    price: String,
    numPages: Number,
  },

  data() {
    return {
      books: [
        {
          title: 'Practical Rust Web Projects',
          isbn: '9781484265888',
          author: 'Shing Lyu',
          publisher: 'Apress',
          price: '$28.75',
          numPages: 256,
        },
        {
          title: 'Using WebPagetest',
          isbn: '9781491902592',
          author: 'Rick Viscomi, Andy Davies, Marcel Duran',
          publisher: 'O\'Reilly Media',
          price: '$25.80',
          numPages: 214,
        },
        {
          title: 'Web Scraping with Python',
          isbn: '9781491910290',
          author: 'Ryan Mitchell',
          publisher: 'O\'Reilly Media',
          price: '$14.00',
          numPages: 256,
        },
        {
          title: 'High Performance Mobile Web',
          isbn: '9781491912553',
          author: 'Maximiliano Firtman',
          publisher: 'O\'Reilly Media',
          price: '$7.00',
          numPages: 326,
        },
      ],
    };
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
