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
      showproduct:false,
      searchbar: ''
    }
  },
  methods:{
    pageChange(page) {
      this.currentpage = page;

    },
    handleCart(product) {
      this.cart.push({ ...product })
  },
  handlesearch(pass){
    this.searchbar = pass
  }
}
}
</script>

<template>
  <Nav @gotoNav="pageChange" @pass="handlesearch" />
  <Home v-if="currentpage === 'Home'" />
  <Products v-if="currentpage === 'Products'" @addCart="handleCart" :search="searchbar"/>
  <InCartproducts v-if="currentpage === 'Cart'" :cartItems="cart"/>
  

</template>
