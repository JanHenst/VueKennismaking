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
          title: "Finders Keepers",
          image: "https://images-na.ssl-images-amazon.com/images/I/71RotfrNfPL.jpg",
          description: "“Wake up, genius.” So announces deranged fan Morris Bellamy to iconic author John Rothstein, who once created the famous character Jimmy Gold and hasn’t released anything since. Morris is livid, not just because his favorite writer has stopped publishing, but because Jimmy Gold ended up as a sellout. Morris kills his idol and empties his safe of cash, but the real haul is a collection of notebooks containing John Rothstein’s unpublished work...including at least one more Jimmy Gold novel. Morris hides everything away—the money and the manuscripts no one but Gold ever saw—before being locked up for another horrific crime. But upon Morris’s release thirty-five years later, he’s about to discover that teenager Pete Saubers has already found the stolen treasure—and no one but former police detective Bill Hodges, along with his trusted associates Holly Gibney and Jerome Robinson, stands in the way of his vengeance...\n" +
                  "\n",
          completed: false
        },
        {
          id: 2,
          title: "The Shining",
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
          title: "IT",
          image: "https://prodimage.images-bn.com/pimages/9781982127794_p0_v3_s550x406.jpg",
          description: "Welcome to Derry, Maine. It’s a small city, a place as hauntingly familiar as your own hometown. Only in Derry the haunting is real.\n" +
                  "\n" +
                  "They were seven teenagers when they first stumbled upon the horror. Now they are grown-up men and women who have gone out into the big world to gain success and happiness. But the promise they made twenty-eight years ago calls them reunite in the same place where, as teenagers, they battled an evil creature that preyed on the city’s children. Now, children are being murdered again and their repressed memories of that terrifying summer return as they prepare to once again battle the monster lurking in Derry’s sewers.\n" +
                  "\n",
          completed: false
        },
        {
          id: 4,
          title: "The Institute",
          image: "https://hachette.imgix.net/books/9781529355406.jpg?auto=compress,format&w=440",
          description: "Deep in the woods of Maine, there is a dark state facility where kids, abducted from across the United States, are incarcerated. In the Institute they are subjected to a series of tests and procedures meant to combine their exceptional gifts - telepathy, telekinesis - for concentrated effect.\n" +
                  "\n" +
                  "Luke Ellis is the latest recruit. He's just a regular 12-year-old, except he's not just smart, he's super-smart. And he has another gift which the Institute wants to use...\n" +
                  "\n" +
                  "Far away in a small town in South Carolina, former cop Tim Jamieson has taken a job working for the local sheriff. He's basically just walking the beat. But he's about to take on the biggest case of his career.\n" +
                  "\n" +
                  "Back in the Institute's downtrodden playground and corridors where posters advertise 'just another day in paradise', Luke, his friend Kalisha and the other kids are in no doubt that they are prisoners, not guests. And there is no hope of escape.\n" +
                  "\n" +
                  "But great events can turn on small hinges and Luke is about to team up with a new, even younger recruit, Avery Dixon, whose ability to read minds is off the scale. While the Institute may want to harness their powers for covert ends, the combined intelligence of Luke and Avery is beyond anything that even those who run the experiments - even the infamous Mrs Sigsby - suspect.",
          completed: false
        },
        {
          id: 5,
          title: "The Stand",
          image: "https://images-na.ssl-images-amazon.com/images/I/81c8No6mSPL.jpg",
          description: "A patient escapes from a biological testing facility, unknowingly carrying a deadly weapon: a mutated strain of super-flu that will wipe out 99 percent of the world’s population within a few weeks. Those who remain are scared, bewildered, and in need of a leader. Two emerge—Mother Abagail, the benevolent 108-year-old woman who urges them to build a peaceful community in Boulder, Colorado; and Randall Flagg, the nefarious “Dark Man,” who delights in chaos and violence. As the dark man and the peaceful woman gather power, the survivors will have to choose between them—and ultimately decide the fate of all humanity.",
          completed: false
        },
        {
          id: 6,
          title: "The Mist",
          image: "https://prodimage.images-bn.com/pimages/9781982103521_p0_v2_s550x406.jpg",
          description: "In the wake of a summer storm, terror descends...David Drayton, his son Billy, and their neighbor Brent Norton join dozens of others and head to the local grocery store to replenish supplies following a freak storm. Once there, they become trapped by a strange mist that has enveloped the town. As the confinement takes its toll on their nerves, a religious zealot, Mrs. Carmody, begins to play on their fears to convince them that this is God’s vengeance for their sins. She insists a sacrifice must be made and two groups—those for and those against—are aligned. Clearly, staying in the store may prove fatal, and the Draytons, along with store employee Ollie Weeks, Amanda Dumfries, Irene Reppler, and Dan Miller, attempt to make their escape. But what’s out there may be worse than what they left behind.",
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
