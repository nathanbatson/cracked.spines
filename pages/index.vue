<template>
  <div>
    <BookClubHeader />
    <NuxtPage />
    <BookClubFooter />
  </div>
</template>

<script setup lang="ts">
import { useBookStore } from '~/stores/books';

const bookStore = useBookStore();

onMounted(() => {
  bookStore.fetchBooks();
  navigateTo('/all')
});
</script>