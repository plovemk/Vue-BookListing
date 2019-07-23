<template id="">
  <!-- <ul> -->
    <!-- <li>{{ book.title }}: {{ book.author }}</li> -->
    <li>{{ book.title}}: {{book.author}}</li>
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
li {
  display: block;
  margin: 0 10px;
}

</style>
