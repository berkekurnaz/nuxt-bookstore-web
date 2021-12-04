<template>
      <div class="container">
            <Navbar />
            <HeaderCategory />
            <Nuxt />
      </div>
</template>

<script>
import Navbar from '@/components/Navbar'
import HeaderCategory from '@/components/HeaderCategory'

export default{
      components: {
            Navbar,
            HeaderCategory
      }
};
</script>
