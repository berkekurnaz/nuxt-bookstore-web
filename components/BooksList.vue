<template>
  <div class="booksList">
    <h3>{{ $t("books.title") }}</h3>
    <span class="viewall">{{ $t("books.view") }}</span>
    <div class="row">
      <div class="col-md-2" v-for="book in books" :key="book.title">
        <Book :book="book" />
      </div>
    </div>
  </div>
</template>

<script>
import Book from "@/components/Book";
import { books } from '@/data/books'
export default {
  components: {
    Book,
  },
  computed: {
    books() {
      return this.$store.state.books.booksList
    }
  }
};
</script>

<style scoped>
  .booksList{
    margin-bottom: 30px;
    position: relative;
  }
  .viewall{
    position: absolute;
    top: 10px;
    right: 10px;
    color: #c2c2c2;
    cursor: pointer;
  }
  h3{
    font-size: 30px;
    font-weight: 600;
    color: var(--color);
  }
</style>