<template>
  <div>
    <div class="cart">
        <div class="image">
          <img src="book2.png" alt="">
        </div>
        <div class="info">
          <h6>{{ book.name }}</h6>
          <p>{{ book.info }}</p>
          <span class="price">$ {{ book.price }}</span>
          <div class="buttons">
            <span class="up"><i class="fa-solid fa-caret-up"></i></span>
            <span>1</span>
            <span class="down"><i class="fa-solid fa-caret-down"></i></span>
          </div>
       </div>
    </div>
  </div>
</template>

<script>
export default {
    props: {
    book: {
      type: Object,
      required: true
    },
  }
}
</script>

<style scoped>
.cart{
    display: flex;
    justify-content: space-evenly;
    align-items: center;
    box-shadow: 3px 8px 9px 1px rgb(215, 215, 212);
    margin: 30px;
    border-radius: 15px;
}
.image img{
    width: 150px;
    padding: 20px;
}
.info h6{
    margin: 0;
    color: rgb(104, 102, 102);
    font-weight: 700;
}
.info p{
    margin: 0;
    color: gray;
}
.price{
    font-size: 18px;
    font-weight: 700;
}
.buttons{
    display: flex;
    align-items: center;
    width: 120px;
    justify-content: space-between;
    margin-top: 5px;
}
.up{
    /* border: 1px solid gray; */
    border-radius: 5px;
    padding: 0px 10px;
    font-size: 25px;
    color: white;
    background-color: rgb(239, 99, 99);
}
.down{
    /* border: 1px solid gray; */
    border-radius: 5px;
    padding: 0px 10px;
    font-size: 25px;
    color: white;
    background-color: rgb(239, 99, 99);
}
</style>