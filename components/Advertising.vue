<template>
      <div class="advertising">
            <div class="column1">
                  <h2>{{ $t("header.main") }}</h2>
                  <p v-html="$t('header.content')"></p>
                  <button>{{ $t("header.button") }}</button>
            </div>
            <div class="column2">
                  <img src="person.png" alt="">
            </div>
      </div>
</template>

<script>
export default{
      
}
</script>

<style scoped>
      .advertising{
            margin-top: 30px;
            margin-bottom: 30px;
            border-radius: 10px;
            height: 250px;
            width: 100%;
            background-color: rgb(243,230,221);
      }
      .column1{
            display: inline-block;
            margin-left: 100px;
            margin-top: 30px;
      }
      h2{
            font-size: 40px;
            color: #423c88;
            margin-top: 10px;
      }
      .column2{
            display: inline-block;
            float: right;
      }
      img{
            width: 330px;
            margin-right: 100px;
            margin-top: 20px;
      }
      button{
            border-radius: 6px;
            border: none;
            background-color: #c2a792;
            color: #fff;
            padding: 10px 20px;
      }
      p{
            color: #bac0c5;
            margin-top: 10px;
            margin-bottom: 20px;
      }
      @media only screen and (max-width: 800px) {
            img{
                  display: none;
            }
            .column1{
                  margin-top: 20px;
                  margin-left: 20px;
            }
      }
</style>