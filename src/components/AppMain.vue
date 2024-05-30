<script>
import Card from "./Card.vue";

export default {
    components: {
        Card,
    },
    data() {
        return {
            products: [
                {
                    id: 1,
                    frontImage: "/assets/img/1.webp",
                    backImage: "/assets/img//1b.webp",
                    brand: "Levi's",
                    name: "Relaxed Fit",
                    price: 29.99,

                    badges: [
                        {
                            type: "tag",
                            value: "Sostenibilità",
                        },
                        {
                            type: "discount",
                            value: "-50%",
                        },
                    ],
                },
                {
                    id: 2,
                    frontImage: "/assets/img/2.webp",
                    backImage: "/assets/img/2b.webp",
                    brand: "Guess",
                    name: "Roses Tee",
                    price: 20.99,
                    
                    badges: [
                        {
                            type: "discount",
                            value: "-30%",
                        },
                    ],
                },
                {
                    id: 3,
                    frontImage: "/assets/img/3.webp",
                    backImage: "/assets/img/3b.webp",
                    brand: "Come Zucchero Filato",
                    name: "Voglia di colori pastello",
                    price: 129.99,
                    
                    badges: [
                        {
                            type: "discount",
                            value: "-30%",
                        },
                    ],
                },
                {
                    id: 4,
                    frontImage: "/assets/img/4.webp",
                    backImage: "/assets/img/4b.webp",
                    brand: "Levi's",
                    name: "Tee Unisex",
                    price: 14.99,
                   
                    badges: [
                        {
                            type: "tag",
                            value: "Sostenibilità",
                        },
                        {
                            type: "discount",
                            value: "-50%",
                        },
                    ],
                },
                {
                    id: 5,
                    frontImage: "/assets/img/5.webp",
                    backImage: "/assets/img/5b.webp",
                    brand: "Maya Deluxe",
                    name: "Stripe Bodice",
                    price: 99.99,
                    
                    badges: [
                        {
                            type: "tag",
                            value: "Sostenibilità",
                        },
                        {
                            type: "discount",
                            value: "-50%",
                        },
                    ],
                },
                {
                    id: 6,
                    frontImage: "/assets/img/6.webp",
                    backImage: "/assets/img/6b.webp",
                    brand: "Esprit",
                    name: "Maglione - Black",
                    price: 29.99,
            
                    badges: [
                        {
                            type: "tag",
                            value: "Sostenibilità",
                        },
                    ],
                },
            ],
        };
    },
};
</script>

<template>
    <div>
        <Card v-for="product in products" :key="product.id" :product="product" />
    </div>
</template>