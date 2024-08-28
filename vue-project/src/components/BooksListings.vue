<script setup>



 import {ref,onMounted} from 'vue'

 const books = ref([]);

 const BookFetching = async () => {
  const result = await fetch("https://freetestapi.com/api/v1/books");
  const data = await result.json();
  console.log(data);
  books.value = data;
};

  onMounted(()=>{


    BookFetching()
  })





</script>


<template>
<h1>BookList</h1>

<ul>
    <li v-for=" book in books" :key="book.id">
{{ book.title }} AND {{ book.author }}

    </li>
</ul>



</template>