<script>
    export default{
        props : {
            products : {
                type : Array,
                required : true,
                default (){
                    return[];
                },
            },
        },
    }
</script>
<template>
    <div>
        <h1>과일 목록</h1>
        <ul>
            <li v-for="(product, index) in products" :key="index">
                <a href="">{{ product.productName }} / {{ product.productPrice }}</a>
            </li>
        </ul>
    </div>
</template>