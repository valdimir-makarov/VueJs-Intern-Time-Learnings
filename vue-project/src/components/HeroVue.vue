<script setup>

import { defineProps } from 'vue';
  


 const props=  defineProps({
 title:{
   type:String,
   default:"my name is Bubban"


 }


   })
</script>




<template>
    <section class="relative bg-blue-600 text-white h-screen flex items-center justify-center">
      <div class="absolute inset-0 overflow-hidden">
        <img
          src="https://via.placeholder.com/1920x1080"
          alt="Hero Background"
          class="w-full h-full object-cover"
        />
      </div>
      <div class="relative z-10 text-center">
        <h1 class="text-5xl font-bold mb-4">{{ props.title }}</h1>
        <p class="text-lg mb-8">Your journey to amazing experiences starts here.</p>
        
      </div>
    </section>
  </template>
  
