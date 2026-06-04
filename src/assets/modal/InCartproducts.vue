<script>
import Transaction from '../../components/Transaction.vue';
export default {
    components: {
        Transaction
    },
    props: {
        cartItems: {
            type: Array
        }
    },
    emits: ['checkout', 'history'],
    data() {
        return {
            showtransaction: false,
            cart: true,
            items: true,
            currentindex: 0,
            checkoutCart: [],
            historyCart:[]
        }
    },
    methods: {
        checkOut() {
            // this.$emit('checkout',  ...product )
            this.checkoutCart.push(...this.cartItems)
            this.showtransaction = true;
            this.cart = false;
            this.showproduct = false;
        },
        purchaseHistory() {
            this.$emit('history', this.historyCart)
            this.historyCart.push(...this.cartItems)
            this.showtransaction = true;
            this.cart = false;
            this.showproduct = false;
        }
    }

}
</script>

<template>
    <div class="px-4 py-4">
        <h1 class="text-rose-500 text-lg font-serif font-semibold">My Orders.</h1>
    </div>
    <div v-if="items">
        <div class="grid grid-cols-4">
            <div v-for="items in cartItems" :key="items.id"
                class="h-50 w-45 bg-white shadow-lg border-1 border-transparent hover:border-pink-500 relative mb-3 mt-4">

                <img class="h-30 w-45  object-fit" :src="items.img" alt="">
                <div class="px-3">
                    <p class="text-rose-500 text-[10px]">{{ items.star }}</p>
                    <p class="text-[10px]">{{ items.name }}</p>
                    <div class="flex justify-between mt-3">
                        <button class="text-[10px] text-rose-500 ">₱{{ items.price }} </button>
                        <p class="text-[10px] text-rose-500">{{ items.sold }} sold</p>
                    </div>
                    <button class="bg-rose-500 text-white text-[8px] font-bold px-3" @click="checkOut">Check
                        Out</button>
                </div>
            </div>
        </div>
    </div>
    <Transaction v-if="showtransaction"  @checkout="checkOut" :checkoutproducts="checkoutCart" @producthistory="purchaseHistory" />
</template>