<template>
  <div id="app">
    <Header />
    <Books v-bind:books="books" v-on:del-book="deleteBook" />
  </div>
</template>

<script>
import Header from './components/layout/Header';
import Books from './components/Books';

export default {
  name: 'app',
  components: {
    Header,
    Books
  },
  data() {
    return {
      books: [
        {
          id: 1,
          title: "Book One",
          completed: false
        },
        {
          id: 2,
          title: "Book Two",
          completed: true
        },
        {
          id: 3,
          title: "Book Three",
          completed: false
        },
        {
          id: 4,
          title: "Book Four",
          completed: false
        },
        {
          id: 5,
          title: "Book Five",
          completed: true
        },
        {
          id: 6,
          title: "Book Six",
          completed: false
        }

      ]
    }
  },
  methods: {
    deleteBook(id) {
      this.books = this.books.filter(book => book.id !== id);
    }
  }
}
</script>

<style>
  * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }

  body {
    font-family: Arial, Helvetica, SansSerif;
    line-height: 1.4;
  }
</style>
