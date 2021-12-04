<template>
  <div>
    <Advertising />
    <BooksList />
    <BooksList />
  </div>
</template>

<script>
import Advertising from '@/components/Advertising'
import BooksList from '@/components/BooksList'

export default {
  layout: 'mainLayout',
  components: {
    Advertising,
    BooksList
  }
}
</script>
