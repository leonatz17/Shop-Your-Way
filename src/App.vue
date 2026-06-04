<script>
import Nav from './components/Nav.vue';
import Home from './components/Home.vue';
import Products from './assets/modal/Products.vue';
import InCartproducts from './assets/modal/InCartproducts.vue';
import Orderhistory from './assets/modal/Orderhistory.vue';


export default {
  components: {
    Nav,
    Home,
    Products,
    InCartproducts,
    Orderhistory


  },
  data() {
    return {
      currentpage: 'Home',
      cart: [],
      showproduct: false,
      searchbar: '',
      checkedout: [],
      purchased:[]

    }
  },

  methods: {
    pageChange(page) {
      this.currentpage = page;

    },
    handleCart(product) {
      this.cart.push({ ...product })
    },
    handlesearch(search) {
      this.searchbar = search;
    },
    handleCheckOut(product) {
      this.checkedout.push({ ...product })

    },
    handlePurchased(product){
      this.purchased.push({... product})
    }

  },
  
}
</script>

<template>
  <div>
    <Nav @gotoNav="pageChange" @passedValue="handlesearch" />
    <Home v-if="currentpage === 'Home'" />
    <Products v-if="currentpage === 'Products'" @addCart="handleCart" :searchBar="searchbar" @checkout="handleCheckOut" />
    <InCartproducts v-if="currentpage === 'Cart'" :cartItems="cart" @history="handlePurchased"/>
    <Orderhistory v-if="currentpage === 'History'"  :History="purchased" />
  </div>
</template>
