<script>
import ProductList from './components/ProductList.vue';


  export default{
    components : {
      ProductList,
    },
    data(){
      return{
        products : [
          {productName : 'Apple', productPrice : '5000', productStock : 50},
          {productName : 'Banana', productPrice : '3500', productStock : 60},
          {productName : 'Melon', productPrice : '6000', productStock : 70},
          {productName : 'StrawBerry', productPrice : '7000', productStock : 80},
          {productName : 'Grape', productPrice : '6500', productStock : 90},
        ]
      };
    },
    mounted(){
      console.log(this.$refs.detail.getList)
    },
  }
</script>

<template>
  <ProductList :products="products"></ProductList>
</template>

<style scoped>
 
</style>