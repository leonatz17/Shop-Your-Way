<script>
export default{
    props:{
        History:{
            type: Array
        },
        
    },
    data (){
        return{

        }
    },
    methods:{
       
    },
    
}

</script>

<template>
    <div class="flex justify-center relative">
        <div class="h-50 w-30 bg-rose-100/20 mt-4 shadow-lg">
            <div class="flex items-center px-3 ">
                <div class="">
                    <img class="h-10 w-10 rounded-full"
                        src="https://wallpapers.com/images/hd/cute-art-young-ponyo-on7j863p5d781wkr.jpg" alt="">
                </div>
                <div class="flex flex-col">
                    <h1 class="text-[13px] text-rose-500 font-serif px-2">Ponyo</h1>
                    <div class="flex">
                        <svg class="w-3 h-3 text-rose-500" aria-hidden="true" xmlns="http://www.w3.org/2000/svg"
                            width="24" height="24" fill="none" viewBox="0 0 24 24">
                            <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                d="M10.779 17.779 4.36 19.918 6.5 13.5m4.279 4.279 8.364-8.643a3.027 3.027 0 0 0-2.14-5.165 3.03 3.03 0 0 0-2.14.886L6.5 13.5m4.279 4.279L6.499 13.5m2.14 2.14 6.213-6.504M12.75 7.04 17 11.28" />
                        </svg>
                        <h1 class="text-[8px] text-rose-500 font-serif">Edit Profile</h1>
                    </div>

                </div>
            </div>
            <hr class="text-rose-300">
            <div class="flex flex-col gap-5 mt-4 px-3">
                <div class="flex">
                    <svg class="w-4 h-4 text-rose-500" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" width="24"
                        height="24" fill="none" viewBox="0 0 24 24">
                        <path stroke="currentColor" stroke-width="2"
                            d="M7 17v1a1 1 0 0 0 1 1h8a1 1 0 0 0 1-1v-1a3 3 0 0 0-3-3h-4a3 3 0 0 0-3 3Zm8-9a3 3 0 1 1-6 0 3 3 0 0 1 6 0Z" />
                    </svg>
                    <p class="text-rose-500 font-serif text-[10px]">My Account</p>
                </div>
                <div class="flex">
                    <svg class="w-4 h-4 text-rose-500" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" width="24"
                        height="24" fill="none" viewBox="0 0 24 24">
                        <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                            d="M15 4h3a1 1 0 0 1 1 1v15a1 1 0 0 1-1 1H6a1 1 0 0 1-1-1V5a1 1 0 0 1 1-1h3m0 3h6m-6 5h6m-6 4h6M10 3v4h4V3h-4Z" />
                    </svg>
                    <p class="text-rose-500 font-serif text-[10px]">My Purchases</p>

                </div>
                <div class="flex">
                    <svg class="w-4 h-4 text-rose-500" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" width="24"
                        height="24" fill="none" viewBox="0 0 24 24">
                        <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                            d="M12 5.365V3m0 2.365a5.338 5.338 0 0 1 5.133 5.368v1.8c0 2.386 1.867 2.982 1.867 4.175 0 .593 0 1.292-.538 1.292H5.538C5 18 5 17.301 5 16.708c0-1.193 1.867-1.789 1.867-4.175v-1.8A5.338 5.338 0 0 1 12 5.365ZM8.733 18c.094.852.306 1.54.944 2.112a3.48 3.48 0 0 0 4.646 0c.638-.572 1.236-1.26 1.33-2.112h-6.92Z" />
                    </svg>
                    <p class="text-rose-500 font-serif text-[10px]">Notifications?</p>
                </div>
                <div class="flex">
                    <svg class="w-4 h-4 text-rose-500" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" width="24"
                        height="24" fill="none" viewBox="0 0 24 24">
                        <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                            d="M18.5 12A2.5 2.5 0 0 1 21 9.5V7a1 1 0 0 0-1-1H4a1 1 0 0 0-1 1v2.5a2.5 2.5 0 0 1 0 5V17a1 1 0 0 0 1 1h16a1 1 0 0 0 1-1v-2.5a2.5 2.5 0 0 1-2.5-2.5Z" />
                    </svg>
                    <p class="text-rose-500 font-serif text-[10px]">My Voucher</p>
                </div>
            </div>
        </div>
        <div class="h-10 w-120 bg-white shadow-lg mt-4 ">
            <div class="text-rose-500 text-[12px] font-serif flex justify-between py-2 px-3">
                <button>All</button>
                <button>To Pay</button>
                <button>To Ship</button>
                <button>To Recieve</button>
                <button>Completed</button>
                <button>Cancelled</button>
            </div>
        </div>

        <div v-for="(item,index) in History" class="flex absolute top-14 left-65">
            <div class="h-35 w-50 bg-white shadow-sm flex flex-col justify-start  mt-4  border-b border-rose-300">

                <div class="flex mt-4">
                    <div class="px-2">
                        <img class="h-20 w-30  border-1 border-gray-300 object-fit" :src="item.img" alt="product image">
                    </div>
                    <div class="mt-8">
                        <h1 class="text-rose-500 font-serif text-[12px] text-center">{{ item.name }}</h1>
                    </div>
                </div>
            </div>
            <div class="h-35 w-70 bg-white shadow-sm mt-4 border-b border-rose-300">
                <div class="  flex justify-between px-5  gap-4 text-rose-500 font-serif text-[10px] p-2">
                    <h2>Unit Price</h2>
                    <h2>Qty.</h2>
                    <h2>Item Subtotal</h2>
                </div>
                <div class="flex justify-between px-5  gap-4 text-rose-500 font-serif text-[10px] mt-8">
                    <h1>₱{{ item.price }}</h1>
                    <h1>1</h1>
                    <h1>₱{{ item.price }}</h1>
                </div>
            </div>
        </div>
    </div>
    <div class="h-10 w-120 bg-white shadow-sm ml-65">
        <div class="flex gap-3 justify-end p-3">
            <h1 class="font-serif text-rose-500">Order Total:</h1>
            <h1 class="bg-rose-600 text-white font-serif px-3">₱₱₱</h1>
        </div>
    </div>

</template>