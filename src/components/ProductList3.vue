<script>
import ProductDetail from './ProductDetail.vue'
export default {
    components: {
        ProductDetail,
    },
    props: {
        productList: {
            type: Array,
            Required: true,
            default: () => {
                return [];
            }
        }
    },
    data() {
        return {
            visibleDetail: false,
            selectedProduct: null,
        }
    },
    methods: {
        clickItem(product) {
            if(this.selectedProduct !== null) {
                if(this.selectedProduct.id === product.id) {
                    this.visibleDetail = false;
                    this.selectedProduct = null;
                } else {
                    this.selectedProduct = product;
                }
            } else {
                this.selectedProduct = product;
                this.visibleDetail = true;
            } 
        },
    }
}
</script>
<template>
    <h1>상품 목록</h1>
<table>
    <thead>
        <tr>
            <th>제목</th>
            <th>가격</th>
        </tr>
    </thead>
    <tbody>
        <tr v-for="(product, index) in productList" :key="index" @click="clickItem(product)">
            <td>{{ product.subject }}</td>
            <td>{{ product.price }}</td>
        </tr>
    </tbody>
</table>
<ProductDetail v-if="visibleDetail" :product="selectedProduct" />
</template>
<style scoped>
table {
    width: 300px;
    text-align: center;
    border-top: 1px solid #444444;
    border-collapse: collapse;
}
th, td {
    border-bottom: 1px solid #444444;
    padding: 10px;
}
</style>