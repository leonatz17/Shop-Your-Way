<script>
import Addtocart from './Addtocart.vue';
export default {
    components:{
        Addtocart
    },
    data() {
        return {
            products: [
                {
                    id: 1,
                    img: 'https://cdn.shopify.com/s/files/1/0818/0305/1309/files/Picasso-Gone-Wrogn-Back-Printed-T-Shirt.webp?v=1744697737',
                    name: 'T-shirt Streetwear Fashion',
                    price: '100.00',
                    sold: '120',
                    star: '★ ★ ★ ★(4)'
                },
                {
                    id: 2,
                    img: 'https://worldbalance.com.ph/cdn/shop/files/WBMCREWSOCKS01BLACK_1.jpg?v=1737085522',
                    name: 'Breathable-comfy Socks',
                    price: '80.00',
                    sold: '110',
                    star: '★★★★★(5)'
                },
                {
                    id: 3,
                    img: 'https://ktlystphclothing.com/cdn/shop/products/N.BLUE.png?v=1649598823',
                    name: 'Navy Blue Tailored Pants',
                    price: '200.00',
                    sold: '10',
                    star: '★★★★★(5)'
                },
                {
                    id: 4,
                    img: 'https://beyondthebox.ph/cdn/shop/collections/apple-watch-2.jpg?v=1759943586',
                    name: 'Smart Watch',
                    price: '500.00',
                    sold: '30',
                    star: '★★★★★(5)'
                },
                {
                    id: 5,
                    img: 'https://transferit.com.ph/pcimages/13125776/140026766/12/1/EFEFEF/prod.jpg?b=11429348&v=1768788701&lm=1776927153',
                    name: 'Polo Shirt',
                    price: '350.00',
                    sold: '50',
                    star: '★★★★(4)'
                },
                {
                    id: 6,
                    img: 'https://www.ordinaree.com/cdn/shop/files/DSC_8875.jpg?v=1756703512',
                    name: 'Red Satin Long Dress ',
                    price: '350.00',
                    sold: '50',
                    star: '★★★★(4)'
                },
                 {
                    id: 7,
                    img: 'https://www.aureliaatelier.com/cdn/shop/collections/IMG_7643.jpg?v=1747932359',
                    name: 'Korean Cute Bracelet ',
                    price: '150.00',
                    sold: '60',
                    star: '★★★(4)'
                },
                {
                    id: 8,
                    img: 'https://dynamic.zacdn.com/OdUWnFZeiPZ2a7MGZVDWq9Inweg=/filters:quality(70):format(webp)/https://static-ph.zacdn.com/p/asos-design-0838-8561143-1.jpg',
                    name: 'Mens Trousers ',
                    price: '200.00',
                    sold: '60',
                    star: '★★★(4)'
                },
                {
                    id: 9,
                    img: 'https://r2r.ph/cdn/shop/files/ready-today-convertible-terno-top-black-fashion-rags2riches-575354.png?v=1725674730',
                    name: 'Convertible Top ',
                    price: '300.00',
                    sold: '100',
                    star: '★★★★★(5)'
                },
                {
                    id: 10,
                    img: 'https://bugattishoes.in/cdn/shop/files/322-A9S01-6900-4100.jpg?v=1762412735',
                    name: 'Sneakers',
                    price: '400.00',
                    sold: '150',
                    star: '★★★★★(5)'
                },
                {
                    id: 11,
                    img: 'https://zoo.com.ph/cdn/shop/products/SUM20-1131.jpg?v=1690482472&width=1445',
                    name: 'Ruffled White Dress',
                    price: '450.00',
                    sold: '250',
                    star: '★★★★★(5)'
                },
                {
                    id: 12,
                    img: 'https://m.media-amazon.com/images/I/61Rb+rv0lNL._AC_UY1100_.jpg',
                    name: 'School Bag Large Capacity',
                    price: '550.00',
                    sold: '150',
                    star: '★★★★★(5)'
                },
                {
                    id: 13,
                    img: 'https://contents.mediadecathlon.com/p3143010/k$e194c6c4863f764893eb9c5886e241ed/waterproof-dry-bag-30-l-khaki-decathlon-8584871.jpg',
                    name: 'Waterproof Dry Bag',
                    price: '650.00',
                    sold: '151',
                    star: '★★★★(4)'
                },
                {
                    id: 14,
                    img: 'https://www.drakensberg.de/cdn/shop/files/DRAKENSBERG-Leder-Baumwoll-Reisetasche-Sam-Gruen-Safari-Style-Hauptansicht.jpg?v=1762468738&width=2500',
                    name: 'Vintage Travel Bag',
                    price: '600.00',
                    sold: '100',
                    star: '★★★★★(5)'
                },
                {
                    id: 15,
                    img: 'https://hushpuppies.com.ph/cdn/shop/files/HPW11141_UPLIFT2-BANDSLIDE_TANLEATHERWeb_2.jpg?v=1756048581&width=1214',
                    name: 'Mega Bounce - Women Sandal',
                    price: '650.00',
                    sold: '200',
                    star: '★★★★★(5)'
                },
                {
                    id: 16,
                    img: 'https://hushpuppies.com.ph/cdn/shop/files/HPW11141_UPLIFT2-BANDSLIDE_TANLEATHERWeb_2.jpg?v=1756048581&width=1214',
                    name: 'Mega Bounce - Women Sandal',
                    price: '650.00',
                    sold: '200',
                    star: '★★★★★(5)'
                },


            ],
            currentIndex: 0,
            showproduct: false,
        }
    },
    methods: {
        buyProducts(index) {
            this.currentIndex = index
            this.showproduct = true;
        },
         addCart(product) {
            this.$emit('addCart', { ...product })
            this.showproduct = false;
        
    }
}
}
</script>

<template>
    <div class="grid grid-cols-4 px-10">
        <div v-for="(product, index) in filteredProducts()"
            class="h-50 w-45 bg-white shadow-lg border-1 border-transparent hover:border-pink-500 relative mb-3 mt-4">

            <img class="h-30 w-45  object-cover object-center" :src="product.img" alt="">
            <div class="px-3">
                <p class="text-rose-500 text-[10px]">{{ product.star }}</p>
                <p class="text-[10px]">{{ product.name }}</p>
                <div class="flex justify-between mt-3">
                    <button class="text-[10px] text-rose-500 ">₱{{ product.price }} </button>
                    <svg class="w-4 h-4 text-rose-500 absolute left-13 top-40 cursor-pointer" aria-hidden="true"
                        xmlns="http://www.w3.org/2000/svg" width="24" height="24" fill="none" viewBox="0 0 24 24"
                        @click="buyProducts(index)">
                        <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                            d="M4 4h1.5L8 16m0 0h8m-8 0a2 2 0 1 0 0 4 2 2 0 0 0 0-4Zm8 0a2 2 0 1 0 0 4 2 2 0 0 0 0-4Zm.75-3H7.5M11 7H6.312M17 4v6m-3-3h6" />
                    </svg>

                    <p class="text-[10px] text-rose-500">{{ product.sold }} sold</p>
                </div>
            </div>
        </div>
    </div>
    <Addtocart v-if="showproduct" :selectedproducts="products[currentIndex]" @addToCart="addCart"/>
</template>