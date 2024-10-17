<script>
import ProductList from './components/ProductList.vue';

export default {
    components: {
        ProductList,
    },
    data() {
        return {
            products: [{
                id: 1,
                subject: 'AAA',
                price: 2000,
                stock: 200
            },
            {
                id: 2,
                subject: 'BBB',
                price: 1500,
                stock: 120
            },
            {
                id: 3,
                subject: 'CCC',
                price: 1300,
                stock: 60
            },
            {
                id: 4,
                subject: 'DDD',
                price: 2400,
                stock: 300
            },
            {
                id: 5,
                subject: 'EEE',
                price: 3200,
                stock: 180
            }]
        }
    },
}

</script>
<template>
    <ProductList :productList="products" />
</template>