<template>
 
  <!-- <div>
    {{name }}
  </div> -->
  <div class="product">
    <div class="image">
        <img src="book2.png" alt="">
    </div>
    <div class="info">
        <h6>{{ product.name }}</h6>
        <p>{{ product.info }}</p>
        <div class="priceinfo">
            <span class="price">$ {{ product.price }}</span>
            <span class="button"><i class="fa-solid fa-cart-shopping"></i></span>
        </div>
    </div>
  </div>
</template>

<script>
export default {
    props: {
    product: {
      type: Object,
      required: true
    },
  }
}
</script>

<style scoped>
.product{
    /* border: 1px solid red; */
    border-radius: 15px;
    margin: 40px 0;
    background-color: rgb(229, 228, 228);
}
.image{
    /* border: 1px solid blue; */
    display: grid;
    justify-content: center;

}
.image img{
    width: 250px;
    /* border: 1px solid red; */
}
.info{
    padding: 0 15px;
}
.info h6{
    /* padding: 0; */
    margin: 0;
    color: rgb(69, 67, 67);
}
.info p{
    color: rgb(79, 78, 78);
}
.priceinfo{
    display: flex;
    justify-content: space-between;
    margin-bottom: 15px;
}
.price{
    font-size: large;
    font-weight: 700;
    color: rgb(78, 78, 78);
}
.button{
padding-right: 20px;
font-size: 20px;
cursor: pointer;
color: rgb(96, 95, 95);
}

/* For mobile responsive */
@media (max-width: 767px) {
    .product{
    /* border: 1px solid red; */
    border-radius: 15px;
    margin: 0px 0;
    background-color: rgb(229, 228, 228);
}
    .image{
    /* border: 1px solid blue; */
    width: 100%;
    display: grid;
    justify-content: center;

}
    .image img{
    width: 100px;
    /* border: 1px solid red; */
}
}
</style>