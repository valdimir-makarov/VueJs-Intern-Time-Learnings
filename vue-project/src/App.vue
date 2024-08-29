<script setup>
import Navbar from "@/components/Navbar.vue";
import HeroVue from "@/components/HeroVue.vue";
import BooksListings from "@/components/BooksListings.vue";
import Books from "@/components/Books.vue";
</script>

<template>
  <Navbar />
  <HeroVue title="Hey, welcome to my website" />
  <BooksListings />
  <Books></Books>
</template>
