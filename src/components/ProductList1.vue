<script>
export default {
  props: {
    products: {
      type: Array,
      required: true,
      default() {
        return [];
      },
    },
  },
  methods: {
    selectProduct(product) {
      // 부모 컴포넌트에 선택된 과일 정보를 전달하는 이벤트 발생
      this.$emit('select-product', product);
    },
  },
};
</script>

<template>
  <div>
    <h1>과일 목록</h1>
    <ul>
      <li v-for="(product, index) in products" :key="index">
        <!-- 과일 항목 클릭 시 selectProduct 메서드 호출 -->
        <a href="#" @click="selectProduct(product)">
          {{ product.productName }} / {{ product.productPrice }}
        </a>
      </li>
    </ul>
  </div>
</template>

<style scoped>
/* 스타일 정의 가능 */
</style>