<template id="">
  <!-- <ul> -->
    <!-- <li>{{ book.title }}: {{ book.author }}</li> -->
    <li style="" v-for="book in books">{{ book.title}}: {{book.author}}</li>
  <!-- </ul> -->
</template>
<script type="text/javascript">
  export default {
    name: 'BookItem',
    props: [
      'book'
    ]
  }
</script>
<style media="screen">


</style>
