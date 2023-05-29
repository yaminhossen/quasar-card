<template>
    <div class="products">
        <product v-for="(item, index) in items" :key="index" 
        :product="item"></product>
    </div>
</template>

<script>
import Product from './Product.vue';
let items = [
    { name: 'Water bottle', price: '9.99', info:'This is the best product and the best quality', img:'image1.png' },
    { name: 'Water bottle', price: '9.99', info:'This is the best product and the best quality', img:'image1.png' },
    { name: 'Water bottle', price: '9.99', info:'This is the best product and the best quality', img:'image1.png' },
    { name: 'Water bottle', price: '9.99', info:'This is the best product and the best quality', img:'image1.png' },
]
export default {



    components: {
        Product
    },

    setup() {

        return {
            items: items,
        }
    }
}
</script>

<style scoped>
.products {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 50px;
    /* padding: 0 140px; */
}
/* For mobile responsive */
@media (max-width: 767px) {
    .products {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 20px;
    padding: 0 20px;
    margin-top: 20px;
}
}
</style>