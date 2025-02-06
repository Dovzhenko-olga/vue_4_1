<template>
<h3>Останні переглянуті товари</h3>
  <div class="list">
<last-rewieved-item v-for="item in productList" :key="item.id" :product="item" :heartLink="heartLink" :cartLink="cartLink"/>

  </div>
</template>

<script>
import LastRewievedItem from "./LastRewievedItem.vue";
  export default {
    name: 'LastRewievedList',
    components: {
      LastRewievedItem,
    },
    data() {
      return {
        heartLink: require('@/assets/heart.jpg'),
        cartLink: require('@/assets/shopping.png'),
        productList: [
          {
            id:1,
            title:'Маршрутизатор TP-Link Archer AX55 Pro',
            price: 3299,
            salePrice: null,
            img: require('@/assets/archer.webp'),
            link: 'https://rozetka.com.ua/ua/archer-ax55-pro/p446219669/',
            isAvailable: true,
          },
          {
            id:2,
            title:'Ігрова поверхня карта світу RZTK Map 900 x 400 x 4 мм',
            price: 399,
            salePrice: null,
            img: require('@/assets/map.webp'),
            link: 'https://hard.rozetka.com.ua/ua/rztk_gmm_9040/p330384193/',
            isAvailable: false,
          },
          {
            id:3,
            title:'Дриль-шурупокрут акумуляторний RZTK RD 1220Li',
            price: 1395,
            salePrice: 1199,
            img: require('@/assets/rztk.webp'),
            link: 'https://rozetka.com.ua/ua/rztk_rd_1220li/p252152001/',
            isAvailable: true,
          },
        ]
      }
    },
  }
</script>

<style lang="css" scoped>
.list{
  display: flex;
}
</style>