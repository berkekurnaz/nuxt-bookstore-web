<template>
  <div class="navbar">
    <h1 class="title">{{ $t("navbar.title") }}</h1>
    <div class="middleArea">
      <input type="text" :placeholder="$t('navbar.placeholder')" />
    </div>
    <div class="rightArea">
      <span>
        <img src="heart.png" width="20px" alt="" />
      </span>
      <span>
        <img src="lamp.png" @click="switchTheme()" width="25px" alt=""/>
      </span>
      <span>
        <nuxt-link class="nuxt-link" :to="switchLocalePath('tr')">TR</nuxt-link>
      </span>
      <span>/</span>
      <span>
        <nuxt-link class="nuxt-link" :to="switchLocalePath('en')">EN</nuxt-link>
      </span>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    switchTheme(){
      console.log(this.$colorMode.preference)
      if(this.$colorMode.preference == 'light') {
        this.$colorMode.preference = 'dark'
      }else {
        this.$colorMode.preference = 'light'
      }
    }
  }
};
</script>

<style scoped>
.navbar {
  margin-top: 30px;
  margin-bottom: 30px;
}
.title {
  display: inline-block;
  font-size: 24px;
  vertical-align: middle;
  color: var(--color);
}
.nuxt-link{
  text-decoration: none;
  color: var(--color);
}
.middleArea {
  display: inline-block;
}
.rightArea {
  display: inline-block;
}
.rightArea span {
  vertical-align: middle;
  cursor: pointer;
  color: var(--color);
}
input {
  width: 500px;
  border-radius: 8px;
  border: none;
  background-color: var(--bginput);
  height: 40px;
  padding-left: 20px;
  font-size: 14px;
}

img{
      margin-right: 20px;
}

@media only screen and (max-width: 1000px){
      input{
            width: 300px;
      }
}

@media only screen and (max-width: 800px) {
  .title{
        display: block;
        font-size: 18px;
        margin-top: 5px;
  }
  input{
        width: 140px;
        padding-left: 5px;
  }
  .middleArea{
        display: block;
  }
  .rightArea{
        display: block;
  }
  .rightArea span{
        font-size: 13px;
  }
  img{
        margin-right: 2px;
        display: none;
  }
}
</style>