
<template id="">
  <div class="">
    <h1>{{ title }}</h1>
      <ul style="">
        <!-- <li style="" v-for="book in books">{{ book.title}}: {{book.author}}</li> -->
        <book-item v-for="book in books" :book="book"></book-item>
      </ul>
      <book-form @addBook='appendBook'></book-form>
  </div>
</template>
<script type="text/javascript">
import BookItem from './BookItem';
import BookForm from './BookForm';
  export default  {
    name: "BookList",
    data(){
      return {
        title: "All Books",
        books: [
          {title: 'Self-Reliance', author: 'Ralph Waldo Emerson'},
          {title: 'American Gods', author: 'Neil Gaiman'},
          {title: 'Amusing Ourselves to Death', author: 'Neil Postman'},
        ]
      };
    },
    components: {
      BookItem,
      BookForm
    },
    methods: {
      appendBook(bookTitle, bookAuthor){
        this.books.push({ title: bookTitle, author: bookAuthor })
      }
    }
  }
</script>
<style media="screen">
  h1, h2 {
    font-weight: normal;
  }
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: block;
  margin: 0 10px;
}
</style>
