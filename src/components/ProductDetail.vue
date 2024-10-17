<script>
export default {
  props: {
    product: {
      type: Object,
      required: true
    }
  }
}
</script>
<template>
    <div v-if="product">
      <h2>과일 상세 정보</h2>
      <p>이름: {{ product.productName }}</p>
      <p>가격: {{ product.productPrice }}원</p>
      <p>재고: {{ product.productStock }}개</p>
    </div>
</template>
  
  <style scoped>
  /* 스타일 정의 가능 */
  </style>
  