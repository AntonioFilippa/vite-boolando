<script>
export default {
    data() {
        return {
            hover: false,
        };
    },
    props: {
        product: {
            type: Object,
        },
    },
};
</script>

<template>
     <div class="card" @mouseover="hover = true" @mouseleave="hover = false">
        
        <img v-if="!hover" :src="product.frontImage" alt="Product Image" class="card-image" />
        <img v-else :src="product.backImage" alt="Product Image" class="card-image" />
        <div class="card-info">
        
            <h3>{{ product.brand }}</h3>
        
            <p>{{ product.name }}</p>
        
            <p class="price">{{ product.price.toFixed(2) }} €</p>
        
            <div class="badges">
        
                <div v-for="(badge, index) in product.badges" :key="index" :class="`badge ${badge.type}`">
        
                    {{ badge.value }}
        
                </div>
        
            </div>
        
        </div>
    
    </div>
</template>

<style scoped lang="scss">
.card {
    border: 1px solid #ddd;
    border-radius: 8px;
    height: 400px;
    margin: 16px;
    width: calc(33% - 32px);
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    transition: transform 0.3s ease-in-out;
    display: inline-block;
    position: relative;
   
    

    &:hover {
        transform: scale(1.05);
        //mostrare immagine backimage al posto di frontimage//

    }

    .card-image {
        border-top-left-radius: 8px;
        border-top-right-radius: 8px;
       position: relative;
        width: 100%;
       object-fit: cover;
    }

    .card-info {
        padding: 12px;

        h3 {
            font-size: 1.2em;
            margin-bottom: 8px;
        }

        p {
            margin-bottom: 4px;
        }

        .price {
            font-weight: bold;
        }

        .badges {
            display: flex;
            gap: 4px;
            postion:absolute;
            font-size: 0.8em;
            top: 10px;
            left: 10px;
            display: flex;
        

           

            .badge {
                padding: 4px;
                border-radius: 4px;
                font-size: 0.8em;
                

                &.tag {
                    background-color: #4caf50;
                    color: white;
                }

                &.discount {
                    background-color: red;
                    color: white;
                }
            }
        }
    }
}
</style>