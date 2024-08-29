<template>
    <h1 class="text-large font-italic">View Jobs Portal</h1>
    <!DOCTYPE html>
  <html lang="en">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Navbar Example</title>
    <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
  </head>
  <body>
    <nav class="bg-gray-800 p-4">
      <div class="container mx-auto flex justify-between items-center">
        <div class="text-white text-xl font-bold">
          <a href="#">MyBrand</a>
        </div>
        <div class="hidden md:flex space-x-4">
          <a href="#" class="text-gray-300 hover:text-white">Home</a>
          <a href="/Booklist" class="text-gray-300 hover:text-white">About</a>
          <a href="#" class="text-gray-300 hover:text-white">Services</a>
          <a href="#" class="text-gray-300 hover:text-white">Contact</a>
        </div>
        <button class="md:hidden text-white">
          <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7" />
          </svg>
        </button>
      </div>
      <div class="md:hidden mt-2 space-y-2">
        <a href="#" class="block text-gray-300 hover:text-white">Home</a>
        <a href="#" class="block text-gray-300 hover:text-white">About</a>
        <a href="#" class="block text-gray-300 hover:text-white">Services</a>
        <a href="#" class="block text-gray-300 hover:text-white">Contact</a>
      </div>
    </nav>
  </body>
  </html>
  
  </template>
  