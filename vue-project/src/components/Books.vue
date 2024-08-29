<template>
    <div>
      <h1>Books List</h1>
      <input v-model="searchTerm" placeholder="Search books..." />
      <button @click="performSearch">Search</button>
  
      <ul>
        <li v-for="book in filteredBooks" :key="book.id">
          {{ book.title }} by {{ book.author }}
        </li>
      </ul>
  
      <p v-if="filteredBooks.length === 0">No books found.</p>
    </div>
  </template>
  
  <script>
  import { ref, computed, onMounted } from 'vue';
  
  export default {
    setup() {
      const books = ref([]);
      const searchTerm = ref('');
      const filteredBooks = ref([]);
  
      const fetchBooks = async () => {
        try {
          const response = await fetch('https://freetestapi.com/api/v1/books');
          const data = await response.json();
          books.value = data.data; 
          filteredBooks.value = books.value; 
        } catch (error) {
          console.error('Error fetching books:', error);
        }
      };
  
      const performSearch = () => {
        filteredBooks.value = books.value.filter(book =>
          book.title.toLowerCase().includes(searchTerm.value.toLowerCase())
        );
      };
  
      onMounted(() => {
        fetchBooks();
      });
  
      return {
        searchTerm,
        filteredBooks,
        performSearch
      };
    }
  };
  </script>
  
  <style scoped>

  </style>
  