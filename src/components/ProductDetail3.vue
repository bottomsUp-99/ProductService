<script>
export default {
    props: {
        product: {
            type: Object,
            Required: true,
            default: () => {
                return {};
            }
        }
    },
}
</script>
<template>
    <h2>상품 상세 정보</h2>
    <p>상품명: {{ product.subject }}</p>
    <p>가격: {{ product.price }}</p>
    <p>재고: {{ product.stock }}</p>
</template>