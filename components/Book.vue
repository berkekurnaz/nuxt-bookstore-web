<template>
      <div class="book">
            <img src="https://i2-prod.walesonline.co.uk/incoming/article6890072.ece/ALTERNATES/s615b/hp1.jpg" width="100%" alt="">
            <h4>Harry Potter</h4>
            <h5>J.K Rowling</h5>
            <div class="rates">
                  <span>icon</span>
            </div>
      </div>
</template>

<script>
export default{
      
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