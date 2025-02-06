<template>
  <div>
    <h2>Списки порівнянь</h2>
    <hr>
    <h4>Мобільні телефони</h4>
    <span>Кількість товарів: {{telList.length}}</span>
    <div>
      <template v-for="tel in telList" :key="tel.id">
      <img alt="tel" :src="tel.link">
    </template>
    </div>
<hr>
  </div>
</template>

<script>
  export default {
    name:'ComparisonComp',
    data() {
      return {
        telList: [
          {
            id:'tel1',
            link:require('@/assets/tel1.webp'),
          },
          {
            id:'tel2',
            link:require('@/assets/tel2.webp'),
          },
          {
            id:'tel3',
            link:require('@/assets/tel3.webp'),
          },
        ]
      }
    },
  }
</script>

<style lang="css" scoped>
img{
  width: 50px;
  height: 90px;
  margin-right: 10px;
}

</style>