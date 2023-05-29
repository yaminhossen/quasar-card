<template>
  <div class="carts">
    <cart v-for="(item, index) in items"
     :key="index"
     :book="item"
     ></cart>
  </div>
</template>

<script>
import Cart from './Cart.vue';
let items = [
    { name: 'Water bottle', price: '9.99', info:'This is the best product', img:'book(1).png' },
    { name: 'Water bottle', price: '9.99', info:'This is the best product', img:'book(1).png' },
    { name: 'Water bottle', price: '9.99', info:'This is the best product', img:'book(1).png' },
    { name: 'Water bottle', price: '9.99', info:'This is the best product', img:'book(1).png' },
]
export default {
  components: {
        Cart
    },

    setup() {

        return {
            items: items,
        }
    }
}
</script>

<style scoped>
.carts{
  display: grid;
  grid-template-columns: repeat(2, 1fr);
}
/* For mobile responsive */
@media (max-width: 767px) {
  .carts{
  display: grid;
  grid-template-columns: repeat(1, 1fr);
}
}

</style>