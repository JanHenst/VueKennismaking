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
          image: "https://prodimage.images-bn.com/pimages/9781982103521_p0_v2_s550x406.jpg",
          description: "#1 New York Times bestselling author Stephen King’s terrifying novella about a town engulfed in a dense, mysterious mist as humanity makes its last stand against unholy destruction—originally published in the acclaimed short story collection Skeleton Crew and made into a TV series, as well as a feature film starring Thomas Jane and Marcia Gay Harden.",
          completed: false
        },
        {
          id: 2,
          title: "Book Two",
          image: "https://cdn.waterstones.com/bookjackets/large/9781/4447/9781444720723.jpg",
          description: "One of the true classics of horror fiction, The Shining is regarded as one of Stephen King's masterpieces.\n" +
                  "\n" +
                  "Danny is only five years old, but in the words of old Mr Hallorann he is a 'shiner', aglow with psychic voltage. When his father becomes caretaker of the Overlook Hotel, Danny's visions grow out of control.\n" +
                  "\n" +
                  "As winter closes in and blizzards cut them off, the hotel seems to develop a life of its own. It is meant to be empty. So who is the lady in Room 217 and who are the masked guests going up and down in the elevator? And why do the hedges shaped like animals seem so alive?\n" +
                  "\n" +
                  "Somewhere, somehow, there is an evil force in the hotel - and that, too, is beginning to shine...",
          completed: false
        },
        {
          id: 3,
          title: "Book Three",
          image: "https://prodimage.images-bn.com/pimages/9781982103521_p0_v2_s550x406.jpg",
          description: "dit is een boek geschrevendit is een boek geschrevendit is een boek geschrevendit is een boek geschrevendit is een boek geschrevendit is een boek geschrevendit is een boek geschreven",
          completed: false
        },
        {
          id: 4,
          title: "Book Four",
          image: "https://prodimage.images-bn.com/pimages/9781982103521_p0_v2_s550x406.jpg",
          description: "dit is een boek geschrevendit is een boek geschrevendit is een boek geschrevendit is een boek geschrevendit is een boek geschrevendit is een boek geschrevendit is een boek geschreven",
          completed: false
        },
        {
          id: 5,
          title: "Book Five",
          image: "https://prodimage.images-bn.com/pimages/9781982103521_p0_v2_s550x406.jpg",
          description: "dit is een boek geschrevendit is een boek geschrevendit is een boek geschrevendit is een boek geschrevendit is een boek geschrevendit is een boek geschrevendit is een boek geschreven",
          completed: false
        },
        {
          id: 6,
          title: "Book Six",
          image: "https://prodimage.images-bn.com/pimages/9781982103521_p0_v2_s550x406.jpg",
          description: "dit is een boek geschrevendit is een boek geschrevendit is een boek geschrevendit is een boek geschrevendit is een boek geschrevendit is een boek geschrevendit is een boek geschreven",
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
