<script>
import ProductList from './components/ProductList.vue';
import ProductDetail from './components/ProductDetail.vue';

export default {
  components: {
    ProductList,
    ProductDetail,
  },
  data() {
    return {
      products: [
        { productName: 'Apple', productPrice: '5000', productStock: 50 },
        { productName: 'Banana', productPrice: '3500', productStock: 60 },
        { productName: 'Melon', productPrice: '6000', productStock: 70 },
        { productName: 'StrawBerry', productPrice: '7000', productStock: 80 },
        { productName: 'Grape', productPrice: '6500', productStock: 90 },
      ],
      selectedProduct: null, // 선택된 과일 정보
    };
  },
  methods: {
    setSelectedProduct(product) {
      // 선택된 과일 정보를 저장
      this.selectedProduct = product;
    },
  },
};
</script>

<template>
  <div>
    <ProductList :products="products" @select-product="setSelectedProduct" />
    <ProductDetail v-if="selectedProduct" :product="selectedProduct" />
  </div>
</template>
<style scoped>
</style>