<script>
import Nav from './components/Nav.vue';
import Home from './components/Home.vue';
import Products from './assets/modal/Products.vue';
import InCartproducts from './assets/modal/InCartproducts.vue';



export default {
  components: {
    Nav,
    Home,
    Products,
    InCartproducts,


  },
  data() {
    return {
      currentpage: 'Home',
      cart: [],
      showproduct: false,
      searchbar: '',
      checkedout: []

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

    }

  }
}
</script>

<template>
  <Nav @gotoNav="pageChange" @passedValue="handlesearch" />
  <Home v-if="currentpage === 'Home'" />
  <Products v-if="currentpage === 'Products'" @addCart="handleCart" :searchBar="searchbar" @checkout="handleCheckOut" />
  <InCartproducts v-if="currentpage === 'Cart'" :cartItems="cart" />



</template>
