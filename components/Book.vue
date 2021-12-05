<template>
      <div class="book">
            <img :src="book.image" width="100%" alt="">
            <h4>{{ book.title }}</h4>
            <h5>{{ book.author }}</h5>
            <div class="rates">
                  <span>icon</span>
            </div>
      </div>
</template>

<script>
export default{
      props: ['book']
}
</script>

<style scoped>
      .book{
            display: inline-block;           
            padding-top: 10px;
      }
      img{
            border-radius: 4px;
      }
      h4{
            margin-top: 15px;
            font-weight: 600;
            font-size: 21px;
            color: var(--color);
      }
      h5{
            font-weight: 400;
            font-size: 15px;
            color: #c2c2c2;
      }
</style>