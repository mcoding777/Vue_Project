<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <div class="menu">
    <a v-for="(menu, index) in menus" :key="index">{{menu}}</a>
  </div>
  <h1>Vue 원룸</h1>
  <div v-for="(product, index) in products" :key="index">
    <h4>{{product.name}} 원룸</h4>
    <p>{{product.price}} 만원</p>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      products: [{
        name: '역삼동',
        price: '50',
      }, {
        name: '강남동',
        price: '70',
      }, {
        name: '개포동',
        price: '60',
      }],
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
