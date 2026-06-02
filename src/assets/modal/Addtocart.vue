<script>
export default {
    props: {
        selectedproducts: {
            type: Object
        }
    },
    emits:['addToCart'],
    methods: {
        cart() {
            this.$emit('addToCart', this.selectedproducts)
        }
    }
}
</script>

<template>
    <div class="max-w-md w-full fixed top-5 left-50 z-300">
        <div class="bg-white rounded-2xl shadow-2xl overflow-hidden hover:shadow-3xl  ">
            <div class="relative">
                <div class="absolute inset-0 bg-gradient-to-br from-purple-400 to-indigo-600 opacity-75"></div>
                <img :src="selectedproducts.img" alt="" class="w-full h-50 object-fill object-center relative z-10">
                <div
                    class="absolute top-4 right-4 bg-gray-100 text-xs font-bold px-3 py-2 rounded-full z-20 transform rotate-12">
                    NEW</div>
            </div>
            <div class="p-3">
                <h2 class="text-lg font-bold text-rose-500 mb-2">{{ selectedproducts.name }}</h2>

                <div class="flex items-center justify-between mb-4">
                    <span class="text-xl font-bold text-rose-500">₱{{ selectedproducts.price }}</span>
                    <div class="flex items-center">

                        <span class="ml-1 text-rose-500">{{ selectedproducts.star }}</span>
                    </div>
                </div>
                <button class="w-full bg-rose-600 text-white font-bold py-1 px-3 rounded-lg hover:bg-rose-700
       transition duration-300 ease-in-out transform hover:-translate-y-1 hover:shadow-lg" @click="cart">
                    Add to Cart
                </button>
            </div>
        </div>
    </div>
    <div class="bg-black w-full h-screen opacity-5 absolute top-0">

    </div>
</template>