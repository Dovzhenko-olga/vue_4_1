<template>
  <div class="item">
<img class="heart" :src="heartLink" alt="heart">
<a class="mainLink" :href="product.link" target="_blank" rel="noopener noreferrer">
  <img class="mainImg" :src="product.img" alt="product.title">
</a>
<a class="mainLink" :href="product.link" target="_blank" rel="noopener noreferrer">
<h5>{{product.title}}</h5>
</a>
<span class="response">Залишити відгук</span>
<span class="available" v-if="product.isAvailable">Є в наявності</span>
<span class="available absent" v-else>Немає в наявності</span>
<template v-if="product.salePrice">
<span class="inSale">{{product.price}} ₴</span>
<span class="price sale">{{product.salePrice}} ₴</span></template>
<span class="price" v-else>{{product.price}} ₴</span>
<img class="cart" :src="cartLink" alt="cart">
  </div>
</template>

<script>
  export default {
    name: 'LastRewievedItem',
    props: {
      heartLink: {
        type: String,
        required: true,
      },
      cartLink: {
        type: String,
        required: true,
      },
      product: {
			type: Object,
			required: true,
		},
    },
  }
</script>

<style lang="css" scoped>
.item{
  position: relative;
  display: flex;
  flex-direction: column;
  margin-right: 20px;
  width: 140px;
}
.heart{
  position: absolute;
  top: 10px;
  right: 10px;
  width: 15px;
  height: 15px;
}
.mainLink{
  display: block;
  margin: 0 auto;
  color: rgb(79, 77, 77);
  text-decoration: none;


}
    mainLink:visited {
      text-decoration: none;
    }
.mainImg{
  object-fit: contain;
  width: 70px;
  height: 100px;
}
.response{
  position: relative;
  padding-left: 15px;
  font-size: 12px;
}
.response::before {
  content: ''; 
  position: absolute;
  left: 3px;
  top: 3px;
  width: 10px;
  height: 10px;
  background-image: url('@/assets/response.png');
  background-size: 10px 10px;
    }
.available{
  font-size: 12px;
  color: green;
}
.absent{
  color: gray;
}
.price{
  font-weight: bold;
}
.inSale{
  font-size: 13px;
  color: gray;
  text-decoration: line-through;
}
.sale{
  color: red;
}
.cart{
  position: absolute;
  bottom: 5px;
  right: 10px;
  width: 20px;
  height: 20px;
}
</style>