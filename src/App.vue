<script >
import Nav from './components/Nav.vue';
import Home from './components/Home.vue';
import Products from './assets/modal/Products.vue';
import InCartproducts from './assets/modal/InCartproducts.vue';


export default{
  components:{
    Nav,
    Home,
    Products,
    InCartproducts
  
  },
  data (){
    return{
      currentpage: 'Home',
      cart:[],
      showproduct:false
    }
  },
  methods:{
    pageChange(page) {
      this.currentpage = page;

    },
    handleCart(product) {
      this.cart.push({ ...product })
  }
}
}
</script>

<template>
  <Nav @gotoNav="pageChange"/>
  <Home v-if="currentpage === 'Home'" />
  <Products v-if="currentpage === 'Products'" @addCart="handleCart" />
  <InCartproducts v-if="currentpage === 'Cart'" :cartItems="cart"/>
  

</template>
