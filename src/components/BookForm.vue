<template id="">
  <form class="" action="#" method="post" v-on:submit.prevent="bookSubmit(bookTitle, bookAuthor)">
    <input type="text" name="title" value="" placeholder="Book Title" v-model="bookTitle">
    <input type="text" name="author" value="" placeholder="Book Author" v-model="bookAuthor">
    <button type="submit" name="button" >Add Book</button>
  </form>
</template>
<script type="text/javascript">
  export default {
    methods: {
      bookSubmit(bookTitle, bookAuthor) {
        this.$emit('addBook', bookTitle, bookAuthor);
      }
    },
    name: 'BookForm',
    props: [
      'books'
    ],
    data(){
      return {
        bookTitle: '',
        bookAuthor: ''
      }
    }
  }
</script>
<style media="screen">

</style>
