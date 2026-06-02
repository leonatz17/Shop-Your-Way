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
    data() {
        return {
            showtransaction: false,
            cart: true
        }
    },
    methods: {
        transactionPage() {
            this.showtransaction = true;
            this.cart = false;
        }
    }

}
</script>

<template>

    <div v-if="cart">
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
                    <button class="bg-rose-500 text-white text-[8px] font-bold px-3" @click="transactionPage">Check
                        Out</button>
                </div>
            </div>
        </div>
    </div>
    <Transaction v-if="showtransaction" />
</template>