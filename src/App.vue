<template>
  <div class="menu">
    <a v-for="menu in menus" :key="menu">{{menu}}</a>
  </div>
  <img alt="Vue logo" src="./assets/logo.png" />
  <h1>Vue 원룸</h1>
  <div>
    <h4>{{products[0]}} 원룸</h4>
    <p>50 만원</p>
  </div>
  <div>
    <h4>{{products[1]}} 원룸</h4>
    <p>{{price2}} 만원</p>
  </div>
  <div>
    <h4>{{products.at(-1)}} 원룸</h4>
    <p>{{price2}} 만원</p>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      products: ['역삼동', '강남동', '개포동'],
      menus: ['Home', 'Products', 'About']
    }
  },
  components: {},
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.menu {
  background: darkslateblue;
  padding: 15px;
  border-radius: 5px;
}

.menu a {
  color: white;
  padding: 0 100px;
}

</style>
