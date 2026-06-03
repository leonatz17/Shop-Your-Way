<script>
export default {
    props: {
        checkoutproducts: {
            type: Object
        }
    },
    data() {
        return {
            order: true,
        }
    },
    emits: ['checkout'],
    methods: {
        checkOut() {
            this.$emit('checkout')
        },
        // placeOrder() {
        //     this.order = false;
        // }
    }
}
</script>

<template>
    <div >
        <div  class="h-15 w-full bg-white border-b border-rose-500">
            <h1 class="text-xl text-rose-500 font-serif p-5">Check Out</h1>
        </div>
        <div class="flex flex-col justify-center items-center">
            <div class="h-15 w-170 bg-white shadow-lg/10">
                <h1 class="text-sm p-2 text-rose-500 font-serif">Delivery Address</h1>
                <h1 class="text-sm text-rose-500 font-serif px-2">London</h1>
            </div>
        </div>
        <div v-for="checked in checkoutproducts" class="flex justify-center">
            <div class="h-35 w-80 bg-white shadow-lg/10 flex flex-col justify-start  mt-4  border-b border-rose-300">
                <div>
                    <h2 class="text-[10px] p-2 text-rose-500 font-serif">Products Ordered</h2>
                </div>
                <div class="flex">
                    <div class="px-2">
                        <img class="h-20 w-30  border-1 border-gray-300 object-fit" :src="checked.image" alt="">
                    </div>
                    <div class="mt-8">
                        <h1 class="text-rose-500 font-serif text-[12px] text-center">{{ checked.name }}</h1>
                    </div>
                </div>
            </div>
            <div class="h-35 w-90 bg-white shadow-lg/10 mt-4 border-b border-rose-300">
                <div class="  flex justify-between px-5  gap-4 text-rose-500 font-serif text-[10px] p-2">
                    <h2>Unit Price</h2>
                    <h2>Qty.</h2>
                    <h2>Item Subtotal</h2>
                </div>
                <div class="flex justify-between px-5  gap-4 text-rose-500 font-serif text-[10px] mt-8">
                    <h1>₱ {{ checked }}</h1>
                    <h1>1</h1>
                    <h1>₱ 200.00</h1>
                </div>
            </div>
        </div>
        <div class="flex justify-center mt-3">
            <div class="h-10 w-80 bg-white shadow-lg/10">
                <div
                    class="flex  justify-between text-[10px] px-3 font-serif text-rose-500 p-3 border-b border-rose-300 ">
                    <h1>E-Invoice</h1>
                    <h1 class="text-gray-400">Request Now</h1>
                </div>

            </div>
            <div class="h-10 w-90 bg-white shadow-lg flex justify-between px-4  border-b border-rose-300">
                <div class="flex text-rose-500 p-3 ">
                    <svg class="w-5 h-4 text-rose-500" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" width="24"
                        height="23" fill="none" viewBox="0 0 24 24">
                        <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                            d="M18.5 12A2.5 2.5 0 0 1 21 9.5V7a1 1 0 0 0-1-1H4a1 1 0 0 0-1 1v2.5a2.5 2.5 0 0 1 0 5V17a1 1 0 0 0 1 1h16a1 1 0 0 0 1-1v-2.5a2.5 2.5 0 0 1-2.5-2.5Z" />
                    </svg>
                    <p class="text-[10px] font-serif ">Shop Voucher</p>
                </div>
                <div class="p-2">
                    <button class="text-rose-600 text-[10px] font-serif ">Select Voucher</button>
                </div>
            </div>
        </div>
        <div class="flex justify-center">
            <div class="h-50 w-170 bg-white shadow-lg/10">
                <div class="h-15 w-170 border-b border-rose-300 flex justify-between">
                    <div>
                        <h1 class="text-md font-serif text-rose-500 p-3">Payment Method</h1>
                    </div>
                    <div class="flex gap-2 p-5">
                        <h1 class="text-[10px] font-serif text-rose-500">Cash On Delivery</h1>
                        <h1 class="text-[10px] font-serif text-rose-500">Change</h1>
                    </div>
                </div>
                <div class="h-20 bg-rose-100/50 w-170 flex justify-end p-6 gap-7">
                    <div class="text-[10px] text-rose-500 font-serif">
                        <p>Merchandise Subtotal:</p>
                        <p>Shipping Subtotal:</p>
                        <p>Total Payment:</p>
                    </div>
                    <div class="text-[10px] text-rose-500 font-serif">
                        <p>₱</p>
                        <p>₱</p>
                        <p>₱</p>
                    </div>

                </div>
                <div class="flex justify-end py-5 px-5">
                    <button class="bg-rose-600 font-serif text-[15px] text-white px-3">Place
                        Order</button>
                </div>
            </div>
        </div>
    </div>





</template>