
<template id="">
  <div class="">
    <h1>{{ title }}</h1>
      <ul style="list-style-type: none;padding: 0;display: block; margin: 0 10px;">
        <li v-for="books in books">{{ books.title}}: {{books.author}}</li>
      </ul>

  </div>
</template>
<script type="text/javascript">
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
    }
  }
</script>
<style media="screen">
  h1, h2 {
    font-weight: normal;
  }


</style>
