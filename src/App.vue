<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <div class="menu">
    <a v-for="(menu, index) in menus" :key="index">{{menu}}</a>
  </div>
  <h1>Vue 원룸</h1>
  <div v-for="(product, index) in products" :key="index" class="room-div">
    <img v-bind:src="require('./assets/' + product.img)" alt="원룸 이미지" class="room-img" />
    <h4>{{product.name}} 원룸</h4>
    <p>{{product.price}} 만원</p>
    <button v-on:click="handleClick(index)">허위매물신고</button> <span>신고수 : {{product.declaration}}</span>
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
        declaration: 0,
        img: 'room0.jpg',
      }, {
        name: '강남동',
        price: '70',
        declaration: 0,
        img: 'room1.jpg',
      }, {
        name: '개포동',
        price: '60',
        declaration: 0,
        img: 'room2.jpg',
      }],
      menus: ['Home', 'Products', 'About'],
    }
  },
  methods: {
    handleClick(index) {
      this.products[index].declaration++
      console.log('더하기')
    },
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

.room-div {
  margin-bottom: 80px;
}

.room-img {
  width: 500px;
  height: 300px;
  
  margin-top: 50px;
}

</style>
