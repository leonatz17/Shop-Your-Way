<script>
export default{
    data (){
        return{
            searchbar: ''
        }
    },
    methods:{
        navigate(page) {
            this.$emit('gotoNav', page)
        },
        search(){
            this.$emit('pass', this.searchBar)
        }

    },
    // search logic
   
}
</script>

<template>

    <div class="h-20 w-full bg-rose-400 flex relative">
        <div class="flex gap-3 justify-start items-center top-1 px-25 text-white absolute">
            <h1 class="text-[8px] ">Selling Centre |</h1>
            <p class="text-[8px] ">Products |</p>
            <p class="text-[8px] ">Start Selling |</p>
            <p class="text-[8px]  ">Follow us</p> 
            <svg class="w-2 h-2 ring-1 text-white rounded-full" aria-hidden="true"
                xmlns="http://www.w3.org/2000/svg" width="24" height="24" fill="currentColor" viewBox="0 0 24 24">
                <path fill-rule="evenodd"
                    d="M13.135 6H15V3h-1.865a4.147 4.147 0 0 0-4.142 4.142V9H7v3h2v9.938h3V12h2.021l.592-3H12V6.591A.6.6 0 0 1 12.592 6h.543Z"
                    clip-rule="evenodd" />
            </svg>
            <svg class="w-2 h-2 ring-1 rounded-full text-white " aria-hidden="true" xmlns="http://www.w3.org/2000/svg"
                width="24" height="24" fill="none" viewBox="0 0 24 24">
                <path fill="currentColor" fill-rule="evenodd"
                    d="M3 8a5 5 0 0 1 5-5h8a5 5 0 0 1 5 5v8a5 5 0 0 1-5 5H8a5 5 0 0 1-5-5V8Zm5-3a3 3 0 0 0-3 3v8a3 3 0 0 0 3 3h8a3 3 0 0 0 3-3V8a3 3 0 0 0-3-3H8Zm7.597 2.214a1 1 0 0 1 1-1h.01a1 1 0 1 1 0 2h-.01a1 1 0 0 1-1-1ZM12 9a3 3 0 1 0 0 6 3 3 0 0 0 0-6Zm-5 3a5 5 0 1 1 10 0 5 5 0 0 1-10 0Z"
                    clip-rule="evenodd" />
            </svg>

        </div>

        <div class="flex gap-3 items-center absolute top-0 left-130">
            <div class="flex text-white text-[8px]">
                <svg class="w-3 h-3 text-white" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" width="24"
                    height="24" fill="none" viewBox="0 0 24 24">
                    <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                        d="M12 5.365V3m0 2.365a5.338 5.338 0 0 1 5.133 5.368v1.8c0 2.386 1.867 2.982 1.867 4.175 0 .593 0 1.292-.538 1.292H5.538C5 18 5 17.301 5 16.708c0-1.193 1.867-1.789 1.867-4.175v-1.8A5.338 5.338 0 0 1 12 5.365ZM8.733 18c.094.852.306 1.54.944 2.112a3.48 3.48 0 0 0 4.646 0c.638-.572 1.236-1.26 1.33-2.112h-6.92Z" />
                </svg>
                <p>Notifications?</p>
            </div>
            <div class="flex text-white text-[8px] justify-center items-center">
                <svg class="w-3 h-6 text-white" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" width="24"
                    height="24" fill="none" viewBox="0 0 24 24">
                    <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                        d="M9.529 9.988a2.502 2.502 0 1 1 5 .191A2.441 2.441 0 0 1 12 12.582V14m-.01 3.008H12M21 12a9 9 0 1 1-18 0 9 9 0 0 1 18 0Z" />
                </svg>
                <p>Help</p>
            </div>
            <div class="flex text-white text-[8px]">
                <svg class="w-3 h-3 text-white" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" width="24"
                    height="24" fill="none" viewBox="0 0 24 24">
                    <path stroke="currentColor" stroke-linecap="round" stroke-width="2"
                        d="M4.37 7.657c2.063.528 2.396 2.806 3.202 3.87 1.07 1.413 2.075 1.228 3.192 2.644 1.805 2.289 1.312 5.705 1.312 6.705M20 15h-1a4 4 0 0 0-4 4v1M8.587 3.992c0 .822.112 1.886 1.515 2.58 1.402.693 2.918.351 2.918 2.334 0 .276 0 2.008 1.972 2.008 2.026.031 2.026-1.678 2.026-2.008 0-.65.527-.9 1.177-.9H20M21 12a9 9 0 1 1-18 0 9 9 0 0 1 18 0Z" />
                </svg>
                <p>English</p>

            </div>
            <div class="flex text-white text-[8px] justify-center items-center gap-3">
                <button class="font-bold">Sign Up</button>
                <p>|</p>
                <button class="font-bold">Log in</button>
            </div>
        </div>

        <div class="flex justify-between px-25 gap-2 relative">
            <div class="flex justify-center items-center gap-4">
                <img class="h-10 w-10  rounded-full" src="https://i.pinimg.com/736x/c2/af/6e/c2af6e4f4ef43d2afda4b24894d3f3b8.jpg" alt="">
                <h1 class="font-serif font-bold text-md text-white cursor-pointer" @click="navigate('Home')">Shop Your Way</h1>
            </div>
            <!-- search -->
            <div class="flex justify-center items-center  ">
                <input v-model="searchbar" @change="search" class="bg-white h-5 w-90 text-[8px] rounded-[1px] px-1" type="text"
                    placeholder="Sign Up and get 100% off your order">
                <svg class="w-5 h-4 bg-rose-400 text-white absolute left-157 rounded-[1px]  " aria-hidden="true"
                    xmlns="http://www.w3.org/2000/svg" width="24" height="24" fill="none" viewBox="0 0 24 24">
                    <path stroke="currentColor" stroke-linecap="round" stroke-width="2"
                        d="m21 21-3.5-3.5M17 10a7 7 0 1 1-14 0 7 7 0 0 1 14 0Z" />
                </svg>
                <div class="ml-10 ">
                    <svg class="w-6 h-6 text-white" aria-hidden="true"
                        xmlns="http://www.w3.org/2000/svg" width="24" height="24" fill="none" viewBox="0 0 24 24" @click="navigate('Cart')">
                        <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                            d="M5 4h1.5L9 16m0 0h8m-8 0a2 2 0 1 0 0 4 2 2 0 0 0 0-4Zm8 0a2 2 0 1 0 0 4 2 2 0 0 0 0-4Zm-8.5-3h9.25L19 7H7.312" />
                    </svg>

                </div>

            </div>
        </div>
        <button class="text-[10px] absolute text-white top-15 left-85 z-200 border-1 border-transparent hover:border-white px-3 rounded-lg cursor-pointer" @click="navigate('Products')">➜ Shop Now! Get 10% discount on your first order!</button>
    </div>

</template>