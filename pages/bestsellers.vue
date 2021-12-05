<template>
      <div>
            <br>
            <BooksList />
            <BooksList />
      </div>
</template>

<script>
import BooksList from '@/components/BooksList'

export default {
      layout: 'mainLayout',
      components: {
            BooksList
      }
}
</script>