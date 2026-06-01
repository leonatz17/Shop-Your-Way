<script>
export default {
    data() {
        return {
            category: [
                {
                    id: 1,
                    img: 'https://m.media-amazon.com/images/I/41eQmm7YCNL._SL500_.jpg',
                    name: 'Mobiles and Gadgets'
                },
                {
                    id: 2,
                    img: 'https://ozmobiles.com.au/cdn/shop/files/USB-A_Cable_Apple_600x.png?v=1778583112g',
                    name: 'Mobile Accesories'
                },
                {
                    id: 3,
                    img: 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTiOPMiTCuRF7sumM0kuyan2-Xh0Jr1AUYfng&s',
                    name: 'Home Entertainment'
                },
                {
                    id: 4,
                    img: 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQu974mE0tG3jI7uveT4uNNQhjcTqqB5fx2hg&s',
                    name: 'Babies and Kids'
                },
                {
                    id: 5,
                    img: 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTCtXXqP9LBsSi3f0lKf49BQbAh7Mn1-9NuZw&s',
                    name: 'Home and Living'
                },
                {
                    id: 6,
                    img: 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTUpe-30PeigXBus74-BzRV3vx6JmBAAeGHjA&s',
                    name: 'Groceries'
                },
                {
                    id: 7,
                    img: 'https://static.vecteezy.com/system/resources/thumbnails/029/830/133/small_2x/toys-and-car-on-isolated-white-background-ai-generative-photo.jpg',
                    name: 'Toys games and Collectibles'
                },
                {
                    id: 8,
                    img: 'https://static.vecteezy.com/system/resources/thumbnails/029/830/133/small_2x/toys-and-car-on-isolated-white-background-ai-generative-photo.jpg',
                    name: 'Toys games and Collectibles'
                },
                {
                    id: 9,
                    img: 'https://coach.scene7.com/is/image/Coach/cv934_imblk_a0',
                    name: 'Womens Bag'
                },
                {
                    id: 10,
                    img: 'https://n.nordstrommedia.com/is/image/nordstrom/12320322_10_Square-Rectangle_10864932-700_8-5.jpeg?width=240&dpr=2&crop=1280%3A1600%2Coffset-x50%2Coffset-y50',
                    name: 'Womens Accessories'
                },
                {
                    id: 11,
                    img: 'https://littleboxindia.com/cdn/shop/files/Tie_Shoulder_Layered_Ruched_Cami_Dress_In_Pink.jpg?v=1754569211',
                    name: 'Womens Apparel'
                },
                {
                    id: 12,
                    img: 'https://images.verifiedmarketresearch.com/assets/Top-7-personal-care-product-companies-empowering-beauty-and-enhancing-well-being.jpg',
                    name: 'Health and Personal Care'
                },
                {
                    id: 13,
                    img: 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSnREp6Ymxl3_qA3iHaxnIZ8y8JkRtHb_4RcA&s',
                    name: 'Make up and Fragrances'
                },
                {
                    id: 14,
                    img: 'https://winlanddepot.com/cdn/shop/files/MRC-550.jpg?v=1755480242',
                    name: 'Home Appliances'
                },

            ]
        }
    }
}
</script>

<template>
    <div class="flex  justify-center gap-0 relative shadow-lg/40">
        <div class="absolute left-25">
            <img class="h-30 w-120"
                src="https://down-ph.img.susercontent.com/file/ph-11134258-820lc-moni619brshu45@resize_w1594_nl.webp"
                alt="">
        </div>
        <div class="flex flex-col absolute right-23 ">
            <img class="h-15 w-50"
                src="https://down-ph.img.susercontent.com/file/ph-11134258-820lb-mnxyuqyaxhc5ec@resize_w796_nl.webp"
                alt="">
            <img class="h-15 w-50"
                src="https://thumbs.dreamstime.com/b/flash-sale-discount-banner-template-promotion-457855756.jpg"
                alt="">
        </div>
    </div>
    <div class="h-15 w-170 bg-white shadow-lg/20 absolute top-53 left-25 flex justify-between px-10">
        <div class="flex flex-col justify-center items-self">
            <img class="h-8 w-8"
                src="https://down-ph.img.susercontent.com/file/ph-11134258-81ztl-me5k6siqqjnp84@resize_w90_nl.webp"
                alt="">
            <p class="text-[7px] border w-10 border-hidden text-center">Siguradong Mura</p>
        </div>
        <div class="flex flex-col justify-center items-self">
            <img class="h-8 w-8"
                src="https://down-ph.img.susercontent.com/file/ph-11134258-81ztm-mhkdwf4knta9c1@resize_w90_nl.webp"
                alt="">
            <p class="text-[7px] border w-15 border-hidden text-center items-center">Fullfilled by Shop Your Way</p>
        </div>
        <div class="flex flex-col justify-center items-self">
            <img class="h-8 w-8"
                src="https://down-ph.img.susercontent.com/file/ph-11134258-7ra0p-mb4xvtcan4um7d@resize_w90_nl.webp"
                alt="">
            <p class="text-[7px] border w-10 border-hidden text-center items-center">Falsh Deals</p>
        </div>
        <div class="flex flex-col justify-center items-self">
            <img class="h-8 w-8"
                src="https://down-ph.img.susercontent.com/file/ph-11134258-7rase-m2rvxe6tt81eff@resize_w90_nl.webp"
                alt="">
            <p class="text-[7px] border w-20  border-hidden ">Free Shipping and Vouchers</p>
        </div>
        <div class="flex flex-col justify-center ">
            <img class="h-8 w-8 "
                src="https://down-ph.img.susercontent.com/file/ph-50009109-d035ecb829748ba2404c468aa9ead53f@resize_w90_nl.webp"
                alt="">
            <p class="text-[7px] border w-15 border-hidden">Shop your way Beauty</p>
        </div>
    </div>
    <div class="w-170 h-60 bg-white shadow-lg/20 absolute top-50 left-25 flex relative">
        <div class="h-58 w-168 bg-rose-400 flex mt-1 ml-1 rounded-md">
            <div class="ml-60  h-18 ">

                <img class="w-40 h-18 " src="../assets/images/payday.png" alt="">
            </div>
            <div class="absolute top-19 left-3  flex justify-between  w-162 ">

                <h1 class="text-[10px] text-white">ADD TO CART NA!</h1>
                <h1 class="text-[10px] text-white">See More></h1>
            </div>
            <div class="h-35 w-30 bg-white absolute top-23 left-3">
                <p class="bg-rose-400 text-white text-[6px] border w-4 ml-26">-95%</p>
                <img class="h-25 w-30 px-2 "
                    src="https://images.unsplash.com/photo-1660844817855-3ecc7ef21f12?w=600&auto=format&fit=crop&q=60&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxzZWFyY2h8NHx8c21hcnR3YXRjaHxlbnwwfHwwfHx8MA%3D%3D"
                    alt="">
                <h1 class="text-[10px] text-rose-900 text-center py-2">P5,419.00</h1>
            </div>

            <div class="h-35 w-30 bg-white absolute top-23 left-36">
                <p class="bg-rose-400 text-white text-[6px] border w-4 ml-26">-95%</p>
                <img class="h-25 w-30 px-2 "
                    src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRaiixJnjubuauv57AvMRd-VO75S6bZUWdNfw&s"
                    alt="">
                <h1 class="text-[10px] text-rose-900 text-center py-2">P249.00</h1>
            </div>

            <div class="h-35 w-30 bg-white absolute top-23 left-69">
                <p class="bg-rose-400 text-white text-[6px] border w-4 ml-26">-95%</p>
                <img class="h-25 w-30 px-2 "
                    src="https://media.karousell.com/media/photos/products/2026/3/25/cellphone_for_sale_1774421150_d1a73afa_thumbnail.jpg"
                    alt="">
                <h1 class="text-[10px] text-rose-900 text-center py-2">P249.00</h1>
            </div>
            <div class="h-35 w-30 bg-white absolute top-23 left-102 ">
                <p class="bg-rose-400 text-white text-[6px] border w-4 ml-26">-95%</p>
                <img class="h-25 w-30 px-2 "
                    src="https://media.karousell.com/media/photos/products/2026/3/25/cellphone_for_sale_1774421150_d1a73afa_thumbnail.jpg"
                    alt="">
                <h1 class="text-[10px] text-rose-900 text-center py-2">P249.00</h1>
            </div>
            <div class="h-35 w-30 bg-white absolute top-23 left-135 ">
                <p class="bg-rose-400 text-white text-[6px] border w-4 ml-26">-95%</p>
                <img class="h-25 w-30 px-2 "
                    src="https://media.karousell.com/media/photos/products/2026/3/25/cellphone_for_sale_1774421150_d1a73afa_thumbnail.jpg"
                    alt="">
                <h1 class="text-[10px] text-rose-900 text-center py-2">P249.00</h1>
            </div>
        </div>
    </div>
    <div>
        <h1 class="absolute top-137 left-27 z-100 text-[15px] text-gray-500">CATEGORY</h1>
        <div class="h-55 w-170 bg-white shadow-lg/20 absolute top-55 left-25 grid grid-cols-7 relative px-5 py-10">

            <div v-for="categories in category" :key="categories.id">
                <div class="">
                    <div class="h-20 shadow-lg w-18 mb-2 border-1 border-transparent hover:border-rose-500 cursor-pointer">
                        <img class="h-15 w-18" :src="categories.img" alt="">
                        <p class="text-[7px] text-center">{{ categories.name }}</p>
                    </div>
                </div>
            </div>
        </div>
    </div>


</template>